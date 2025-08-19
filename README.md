<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

</head>
<body class="bg-gray-50 text-gray-800 p-6 leading-relaxed">
  <h1 class="text-2xl font-bold mb-6">📘 Guia Rápido de Classes Tailwind CSS</h1>

  <!-- 1. Layout -->
  <section class="mb-8">
    <h2 class="text-xl font-semibold mb-2">📌 1. Layout</h2>
    <table class="min-w-full border border-gray-300 bg-white">
      <thead>
        <tr class="bg-gray-100">
          <th class="border px-4 py-2 text-left">Categoria</th>
          <th class="border px-4 py-2 text-left">Classes Principais</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="border px-4 py-2">Display</td>
          <td class="border px-4 py-2">block, inline, flex, grid, hidden</td>
        </tr>
        <tr>
          <td class="border px-4 py-2">Position</td>
          <td class="border px-4 py-2">static, relative, absolute, fixed, sticky</td>
        </tr>
        <tr>
          <td class="border px-4 py-2">Flexbox</td>
          <td class="border px-4 py-2">flex-row, flex-col, justify-start, justify-center, items-start, items-center, gap-4</td>
        </tr>
        <tr>
          <td class="border px-4 py-2">Grid</td>
          <td class="border px-4 py-2">grid-cols-3, grid-rows-2, gap-4, col-span-2</td>
        </tr>
        <tr>
          <td class="border px-4 py-2">Box Sizing</td>
          <td class="border px-4 py-2">box-border, box-content</td>
        </tr>
      </tbody>
    </table>
  </section>

  <!-- 2. Espaçamento -->
  <section class="mb-8">
    <h2 class="text-xl font-semibold mb-2">📌 2. Espaçamento (Spacing)</h2>
    <table class="min-w-full border border-gray-300 bg-white">
      <thead class="bg-gray-100">
        <tr>
          <th class="border px-4 py-2 text-left">Tipo</th>
          <th class="border px-4 py-2 text-left">Exemplos</th>
        </tr>
      </thead>
      <tbody>
        <tr><td class="border px-4 py-2">Margin</td><td class="border px-4 py-2">m-4, mx-2, my-3, mt-1, mb-8</td></tr>
        <tr><td class="border px-4 py-2">Padding</td><td class="border px-4 py-2">p-4, px-2, py-3, pt-1, pb-8</td></tr>
        <tr><td class="border px-4 py-2">Gap</td><td class="border px-4 py-2">gap-4, gap-x-2, gap-y-3</td></tr>
      </tbody>
    </table>
  </section>

  <!-- 3. Tipografia -->
  <section class="mb-8">
    <h2 class="text-xl font-semibold mb-2">📌 3. Tipografia (Typography)</h2>
    <table class="min-w-full border border-gray-300 bg-white">
      <thead class="bg-gray-100">
        <tr>
          <th class="border px-4 py-2 text-left">Propriedade</th>
          <th class="border px-4 py-2 text-left">Exemplos</th>
        </tr>
      </thead>
      <tbody>
        <tr><td class="border px-4 py-2">Font Size</td><td class="border px-4 py-2">text-xs, text-sm, text-base, text-lg, text-xl</td></tr>
        <tr><td class="border px-4 py-2">Font Weight</td><td class="border px-4 py-2">font-light, font-normal, font-bold</td></tr>
        <tr><td class="border px-4 py-2">Text Align</td><td class="border px-4 py-2">text-left, text-center, text-right</td></tr>
        <tr><td class="border px-4 py-2">Text Color</td><td class="border px-4 py-2">text-black, text-gray-500, text-blue-600</td></tr>
        <tr><td class="border px-4 py-2">Line Height</td><td class="border px-4 py-2">leading-tight, leading-normal</td></tr>
      </tbody>
    </table>
  </section>

  <!-- 4. Cores -->
  <section class="mb-8">
    <h2 class="text-xl font-semibold mb-2">📌 4. Cores (Colors)</h2>
    <table class="min-w-full border border-gray-300 bg-white">
      <thead class="bg-gray-100">
        <tr>
          <th class="border px-4 py-2 text-left">Tipo</th>
          <th class="border px-4 py-2 text-left">Exemplos</th>
        </tr>
      </thead>
      <tbody>
        <tr><td class="border px-4 py-2">Background</td><td class="border px-4 py-2">bg-white, bg-gray-200, bg-blue-500</td></tr>
        <tr><td class="border px-4 py-2">Text</td><td class="border px-4 py-2">text-red-600, text-green-800</td></tr>
        <tr><td class="border px-4 py-2">Border</td><td class="border px-4 py-2">border-gray-300, border-2, border-blue-500</td></tr>
      </tbody>
    </table>
  </section>

  <!-- Repita o mesmo padrão para Bordas, Efeitos, Animações, Responsividade, Estados e Personalização -->
  
  <section class="mt-8">
    <h2 class="text-xl font-semibold mb-2">🔍 Como Ver Todas as Classes?</h2>
    <ul class="list-disc ml-6">
      <li>Documentação Oficial: <a href="https://tailwindcss.com/docs" class="text-blue-600 underline">Tailwind CSS Docs</a></li>
      <li>Autocompletar no VS Code: Instale a extensão <strong>Tailwind CSS IntelliSense</strong></li>
      <li>Lista Completa: Execute <code class="bg-gray-100 px-2 py-1 rounded">npx tailwindcss list</code> no terminal</li>
    </ul>
  </section>

  <section class="mt-8">
    <h2 class="text-xl font-semibold mb-2">📌 Dica Importante</h2>
    <p>Tailwind usa valores relativos (<code>rem</code>, <code>em</code>) ao invés de pixels (<code>px</code>) para garantir acessibilidade. Use <code>px</code> apenas em casos específicos (ex.: <code>w-[10px]</code>).</p>
  </section>
</body>
</html>
