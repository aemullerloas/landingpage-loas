<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Você tem direito ao BPC LOAS?</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 text-gray-900">
  <div class="max-w-4xl mx-auto p-6">
    <div class="bg-white rounded-2xl shadow-lg p-8">
      <h1 class="text-3xl font-bold mb-4 text-center">Descubra se você tem direito ao BPC LOAS</h1>
      <p class="text-lg mb-6 text-center">Milhares de brasileiros deixam de receber um benefício de até <strong>R$ 1.518</strong> por mês — mesmo sem nunca terem contribuído com o INSS.</p>

      <div class="bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 mb-6">
        <p class="font-semibold">Você sabia?</p>
        <p>Pessoas com deficiência ou com 65 anos ou mais podem ter direito ao BPC LOAS e ainda receber valores retroativos acumulados.</p>
      </div>

      <form id="bpcForm" class="space-y-4">
        <label class="block">
          <span class="block font-medium">Nome completo</span>
          <input type="text" id="nome" class="w-full p-2 border border-gray-300 rounded" required>
        </label>
        <label class="block">
          <span class="block font-medium">Telefone com WhatsApp</span>
          <input type="tel" id="telefone" class="w-full p-2 border border-gray-300 rounded" required>
        </label>
        <label class="block">
          <span class="block font-medium">Idade da pessoa que precisa do benefício</span>
          <input type="number" id="idade" class="w-full p-2 border border-gray-300 rounded" required>
        </label>
        <label class="block">
          <span class="block font-medium">Possui algum tipo de deficiência?</span>
          <select id="deficiencia" class="w-full p-2 border border-gray-300 rounded" required>
            <option>Sim</option>
            <option>Não</option>
          </select>
        </label>

        <button type="submit" class="w-full bg-blue-600 text-white p-3 rounded font-bold hover:bg-blue-700 transition">Verificar meu direito</button>
      </form>

      <p class="text-sm text-gray-500 mt-6 text-center">* Este site é informativo. A análise será realizada por um advogado especialista após o envio dos dados.</p>
    </div>
  </div>

  <script>
    document.getElementById('bpcForm').addEventListener('submit', function(e) {
      e.preventDefault();
      
      let nome = document.getElementById('nome').value;
      let telefone = document.getElementById('telefone').value;
      let idade = document.getElementById('idade').value;
      let deficiencia = document.getElementById('deficiencia').value;
      
      let mensagem = `Olá, meu nome é ${nome}. Tenho ${idade} anos, telefone ${telefone}, e ${deficiencia === 'Sim' ? 'possuo' : 'não possuo'} deficiência. Gostaria de verificar se tenho direito ao BPC LOAS.`;
      
      let numeroWhatsApp = "5549999822224";
      let url = `https://wa.me/${numeroWhatsApp}?text=${encodeURIComponent(mensagem)}`;
      
      window.location.href = url;
    });
  </script>
</body>
</html>
