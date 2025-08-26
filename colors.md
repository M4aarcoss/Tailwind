<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabela de Cores HTML</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f5f5f5;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
            padding: 30px;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #eee;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.5rem;
        }

        .description {
            color: #7f8c8d;
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto;
        }

        .controls {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .search-box {
            flex: 1;
            min-width: 250px;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 6px;
            font-size: 16px;
        }

        .color-filter {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .color-btn {
            padding: 8px 16px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .color-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .table-container {
            overflow-x: auto;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
        }

        table {
            width: 100%;
            border-collapse: collapse;
            min-width: 600px;
        }

        th {
            background-color: #34495e;
            color: white;
            padding: 15px;
            text-align: left;
            position: sticky;
            top: 0;
        }

        th:first-child {
            border-top-left-radius: 8px;
        }

        th:last-child {
            border-top-right-radius: 8px;
        }

        td {
            padding: 12px 15px;
            border-bottom: 1px solid #eee;
        }

        tr:hover {
            background-color: #f8f9fa;
        }

        .color-sample {
            display: inline-block;
            width: 20px;
            height: 20px;
            border-radius: 3px;
            margin-right: 8px;
            vertical-align: middle;
            border: 1px solid #ddd;
        }

        .color-name {
            font-weight: 500;
        }

        .color-code {
            font-family: 'Courier New', monospace;
            background-color: #f8f9fa;
            padding: 2px 6px;
            border-radius: 3px;
            font-size: 0.9em;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .controls {
                flex-direction: column;
            }
            
            .search-box {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Tabela de Cores HTML</h1>
            <p class="description">
                Na tabela de cores HTML, você poderá encontrar diversos exemplos de cores com seu código hexadecimal, 
                assim como o nome em inglês e o código RGB, já prontos para copiar diretamente para o seu código HTML/CSS.
            </p>
        </header>

        <div class="controls">
            <input type="text" class="search-box" placeholder="Pesquisar por nome de cor..." id="searchInput">
            <div class="color-filter">
                <button class="color-btn" style="background-color: #ffebee; color: #c62828;" data-category="red">Vermelhos</button>
                <button class="color-btn" style="background-color: #e3f2fd; color: #1565c0;" data-category="blue">Azuis</button>
                <button class="color-btn" style="background-color: #e8f5e9; color: #2e7d32;" data-category="green">Verdes</button>
                <button class="color-btn" style="background-color: #fffde7; color: #f9a825;" data-category="yellow">Amarelos</button>
                <button class="color-btn" style="background-color: #f3e5f5; color: #7b1fa2;" data-category="purple">Roxos</button>
            </div>
        </div>

        <div class="table-container">
            <table id="colorTable">
                <thead>
                    <tr>
                        <th>Amostra</th>
                        <th>Nome da Cor</th>
                        <th>Código Hexadecimal</th>
                        <th>Código RGB</th>
                    </tr>
                </thead>
                <tbody>
                    <!-- As linhas da tabela serão geradas por JavaScript -->
                </tbody>
            </table>
        </div>

        <footer>
            <p>Tabela de cores HTML - Última atualização: 2024</p>
        </footer>
    </div>

    <script>
        // Dados das cores
        const colors = [
            { name: "Black", hex: "#000000", rgb: "(0,0,0)" },
            { name: "Grey11", hex: "#1C1C1C", rgb: "(28,28,28)" },
            { name: "Grey21", hex: "#363636", rgb: "(54,54,54)" },
            { name: "Grey31", hex: "#4F4F4F", rgb: "(79,79,79)" },
            { name: "DimGray", hex: "#696969", rgb: "(105,105,105)" },
            { name: "Gray", hex: "#808080", rgb: "(128,128,128)" },
            { name: "DarkGray", hex: "#A9A9A9", rgb: "(169,169,169)" },
            { name: "Silver", hex: "#C0C0C0", rgb: "(192,192,192)" },
            { name: "LightGrey", hex: "#D3D3D3", rgb: "(211,211,211)" },
            { name: "Gainsboro", hex: "#DCDCDC", rgb: "(220,220,220)" },
            { name: "SlateBlue", hex: "#6A5ACD", rgb: "(106,90,205)" },
            { name: "SlateBlue1", hex: "#836FFF", rgb: "(131,111,255)" },
            { name: "SlateBlue3", hex: "#6959CD", rgb: "(105,89,205)" },
            { name: "DarkSlateBlue", hex: "#483D8B", rgb: "(72,61,139)" },
            { name: "MidnightBlue", hex: "#191970", rgb: "(25,25,112)" },
            { name: "Navy", hex: "#000080", rgb: "(0,0,128)" },
            { name: "DarkBlue", hex: "#00008B", rgb: "(0,0,139)" },
            { name: "MediumBlue", hex: "#0000CD", rgb: "(0,0,205)" },
            { name: "Blue", hex: "#0000FF", rgb: "(0,0,255)" },
            { name: "CornflowerBlue", hex: "#6495ED", rgb: "(100,149,237)" },
            { name: "RoyalBlue", hex: "#4169E1", rgb: "(65,105,225)" },
            { name: "DodgerBlue", hex: "#1E90FF", rgb: "(30,144,255)" },
            { name: "DeepSkyBlue", hex: "#00BFFF", rgb: "(0,191,255)" },
            { name: "LightSkyBlue", hex: "#87CEFA", rgb: "(135,206,250)" },
            { name: "SkyBlue", hex: "#87CEEB", rgb: "(135,206,235)" },
            { name: "LightBlue", hex: "#ADD8E6", rgb: "(173,216,230)" },
            { name: "SteelBlue", hex: "#4682B4", rgb: "(70,130,180)" },
            { name: "LightSteelBlue", hex: "#B0C4DE", rgb: "(176,196,222)" },
            { name: "SlateGray", hex: "#708090", rgb: "(112,128,144)" },
            { name: "LightSlateGray", hex: "#778899", rgb: "(119,136,153)" },
            { name: "Aqua / Cyan", hex: "#00FFFF", rgb: "(0,255,255)" },
            { name: "DarkTurquoise", hex: "#00CED1", rgb: "(0,206,209)" },
            { name: "Turquoise", hex: "#40E0D0", rgb: "(64,224,208)" },
            { name: "MediumTurquoise", hex: "#48D1CC", rgb: "(72,209,204)" },
            { name: "LightSeaGreen", hex: "#20B2AA", rgb: "(32,178,170)" },
            { name: "DarkCyan", hex: "#008B8B", rgb: "(0,139,139)" },
            { name: "Teal", hex: "#008080", rgb: "(0,128,128)" },
            { name: "Aquamarine", hex: "#7FFFD4", rgb: "(127,255,212)" },
            { name: "MediumAquamarine", hex: "#66CDAA", rgb: "(102,205,170)" },
            { name: "CadetBlue", hex: "#5F9EA0", rgb: "(95,158,160)" },
            { name: "DarkSlateGray", hex: "#2F4F4F", rgb: "(47,79,79)" },
            { name: "MediumSpringGreen", hex: "#00FA9A", rgb: "(0,250,154)" },
            { name: "SpringGreen", hex: "#00FF7F", rgb: "(0,255,127)" },
            { name: "PaleGreen", hex: "#98FB98", rgb: "(152,251,152)" },
            { name: "LightGreen", hex: "#90EE90", rgb: "(144,238,144)" },
            { name: "DarkSeaGreen", hex: "#8FBC8F", rgb: "(143,188,143)" },
            { name: "MediumSeaGreen", hex: "#3CB371", rgb: "(60,179,113)" },
            { name: "SeaGreen", hex: "#2E8B57", rgb: "(46,139,87)" },
            { name: "DarkGreen", hex: "#006400", rgb: "(0,100,0)" },
            { name: "Green", hex: "#008000", rgb: "(0,128,0)" },
            { name: "ForestGreen", hex: "#228B22", rgb: "(34,139,34)" },
            { name: "LimeGreen", hex: "#32CD32", rgb: "(50,205,50)" },
            { name: "Lime", hex: "#00FF00", rgb: "(0,255,0)" },
            { name: "LawnGreen", hex: "#7CFC00", rgb: "(124,252,0)" },
            { name: "Chartreuse", hex: "#7FFF00", rgb: "(127,255,0)" },
            { name: "GreenYellow", hex: "#ADFF2F", rgb: "(173,255,47)" },
            { name: "YellowGreen", hex: "#9ACD32", rgb: "(154,205,50)" },
            { name: "OliveDrab", hex: "#6B8E23", rgb: "(107,142,35)" },
            { name: "DarkOliveGreen", hex: "#556B2F", rgb: "(85,107,47)" },
            { name: "Olive", hex: "#808000", rgb: "(128,128,0)" },
            { name: "DarkKhaki", hex: "#BDB76B", rgb: "(189,83,107)" },
            { name: "Goldenrod", hex: "#DAA520", rgb: "(218,165,32)" },
            { name: "DarkGoldenrod", hex: "#B8860B", rgb: "(184,134,11)" },
            { name: "SaddleBrown", hex: "#8B4513", rgb: "(139,69,19)" },
            { name: "Sienna", hex: "#A0522D", rgb: "(160,82,45)" },
            { name: "RosyBrown", hex: "#BC8F8F", rgb: "(188,143,143)" },
            { name: "Peru", hex: "#CD853F", rgb: "(205,133,63)" },
            { name: "Chocolate", hex: "#D2691E", rgb: "(210,105,30)" },
            { name: "SandyBrown", hex: "#F4A460", rgb: "(244,164,96)" },
            { name: "NavajoWhite", hex: "#FFDEAD", rgb: "(255,222,173)" },
            { name: "Wheat", hex: "#F5DEB3", rgb: "(245,222,179)" },
            { name: "BurlyWood", hex: "#DEB887", rgb: "(222,184,135)" },
            { name: "Tan", hex: "#D2B48C", rgb: "(210,180,140)" },
            { name: "MediumSlateBlue", hex: "#7B68EE", rgb: "(123,104,238)" },
            { name: "MediumPurple", hex: "#9370DB", rgb: "(147,112,219)" },
            { name: "BlueViolet", hex: "#8A2BE2", rgb: "(138,43,226)" },
            { name: "Indigo", hex: "#4B0082", rgb: "(75,0,130)" },
            { name: "DarkViolet", hex: "#9400D3", rgb: "(148,0,211)" },
            { name: "DarkOrchid", hex: "#9932CC", rgb: "(153,50,204)" },
            { name: "MediumOrchid", hex: "#BA55D3", rgb: "(186,85,211)" },
            { name: "Purple", hex: "#A020F0", rgb: "(128,0,128)" },
            { name: "DarkMagenta", hex: "#8B008B", rgb: "(139,0,139)" },
            { name: "Fuchsia / Magenta", hex: "#FF00FF", rgb: "(255,0,255)" },
            { name: "Violet", hex: "#EE82EE", rgb: "(238,130,238)" },
            { name: "Orchid", hex: "#DA70D6", rgb: "(218,112,214)" },
            { name: "Plum", hex: "#DDA0DD", rgb: "(221,160,221)" },
            { name: "MediumVioletRed", hex: "#C71585", rgb: "(199,21,133)" },
            { name: "DeepPink", hex: "#FF1493", rgb: "(255,20,147)" },
            { name: "HotPink", hex: "#FF69B4", rgb: "(255,105,180)" },
            { name: "PaleVioletRed", hex: "#DB7093", rgb: "(219,112,147)" },
            { name: "LightPink", hex: "#FFB6C1", rgb: "(255,182,193)" },
            { name: "Pink", hex: "#FFC0CB", rgb: "(255,192,203)" },
            { name: "LightCoral", hex: "#F08080", rgb: "(240,128,128)" },
            { name: "IndianRed", hex: "#CD5C5C", rgb: "(205,92,92)" },
            { name: "Crimson", hex: "#DC143C", rgb: "(220,20,60)" },
            { name: "Maroon", hex: "#800000", rgb: "(128,0,0)" },
            { name: "DarkRed", hex: "#8B0000", rgb: "(139,0,0)" },
            { name: "FireBrick", hex: "#B22222", rgb: "(178,34,34)" },
            { name: "Brown", hex: "#A52A2A", rgb: "(165,42,42)" },
            { name: "Salmon", hex: "#FA8072", rgb: "(250,128,114)" },
            { name: "DarkSalmon", hex: "#E9967A", rgb: "(233,150,122)" },
            { name: "LightSalmon", hex: "#FFA07A", rgb: "(255,160,122)" },
            { name: "Coral", hex: "#FF7F50", rgb: "(255,127,80)" },
            { name: "Tomato", hex: "#FF6347", rgb: "(255,99,71)" },
            { name: "Red", hex: "#FF0000", rgb: "(255,0,0)" },
            { name: "OrangeRed", hex: "#FF4500", rgb: "(255,69,0)" },
            { name: "DarkOrange", hex: "#FF8C00", rgb: "(255,140,0)" },
            { name: "Orange", hex: "#FFA500", rgb: "(255,165,0)" },
            { name: "Gold", hex: "#FFD700", rgb: "(255,215,0)" },
            { name: "Yellow", hex: "#FFFF00", rgb: "(255,255,0)" },
            { name: "Khaki", hex: "#F0E68C", rgb: "(240,230,140)" },
            { name: "AliceBlue", hex: "#F0F8FF", rgb: "(240,248,255)" },
            { name: "GhostWhite", hex: "#F8F8FF", rgb: "(248,248,255)" },
            { name: "Snow", hex: "#FFFAFA", rgb: "(255,250,250)" },
            { name: "Seashell", hex: "#FFF5EE", rgb: "(255,245,238)" },
            { name: "FloralWhite", hex: "#FFFAF0", rgb: "(255,250,240)" },
            { name: "WhiteSmoke", hex: "#F5F5F5", rgb: "(245,245,245)" },
            { name: "Beige", hex: "#F5F5DC", rgb: "(245,245,220)" },
            { name: "OldLace", hex: "#FDF5E6", rgb: "(253,245,230)" },
            { name: "Ivory", hex: "#FFFFF0", rgb: "(255,255,240)" },
            { name: "Linen", hex: "#FAF0E6", rgb: "(250,240,230)" },
            { name: "Cornsilk", hex: "#FFF8DC", rgb: "(255,248,220)" },
            { name: "AntiqueWhite", hex: "#FAEBD7", rgb: "(250,235,215)" },
            { name: "BlanchedAlmond", hex: "#FFEBCD", rgb: "(255,235,205)" },
            { name: "Bisque", hex: "#FFE4C4", rgb: "(255,228,196)" },
            { name: "LightYellow", hex: "#FFFFE0", rgb: "(255,255,224)" },
            { name: "LemonChiffon", hex: "#FFFACD", rgb: "(255,250,205)" },
            { name: "LightGoldenrodYellow", hex: "#FAFAD2", rgb: "(250,250,210)" },
            { name: "PapayaWhip", hex: "#FFEFD5", rgb: "(255,239,213)" },
            { name: "PeachPuff", hex: "#FFDAB9", rgb: "(255,218,185)" },
            { name: "Moccasin", hex: "#FFE4B5", rgb: "(255,228,181)" },
            { name: "PaleGoldenrod", hex: "#EEE8AA", rgb: "(238,232,170)" },
            { name: "MistyRose", hex: "#FFE4E1", rgb: "(255,228,225)" },
            { name: "LavenderBlush", hex: "#FFF0F5", rgb: "(255,240,245)" },
            { name: "Lavender", hex: "#E6E6FA", rgb: "(230,230,250)" },
            { name: "Thistle", hex: "#D8BFD8", rgb: "(216,191,216)" },
            { name: "Azure", hex: "#F0FFFF", rgb: "(240,255,255)" },
            { name: "LightCyan", hex: "#E0FFFF", rgb: "(224,255,255)" },
            { name: "PowderBlue", hex: "#B0E0E6", rgb: "(176,224,230)" },
            { name: "PaleTurquoise", hex: "#E0FFFF", rgb: "(175,238,238)" },
            { name: "Honeydew", hex: "#F0FFF0", rgb: "(240,255,240)" },
            { name: "MintCream", hex: "#F5FFFA", rgb: "(245,255,250)" }
        ];

        // Função para renderizar a tabela
        function renderTable(data) {
            const tbody = document.querySelector('#colorTable tbody');
            tbody.innerHTML = '';
            
            data.forEach(color => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td><span class="color-sample" style="background-color: ${color.hex}"></span></td>
                    <td><span class="color-name">${color.name}</span></td>
                    <td><code class="color-code">${color.hex}</code></td>
                    <td><code class="color-code">${color.rgb}</code></td>
                `;
                tbody.appendChild(row);
            });
        }

        // Função de pesquisa
        function setupSearch() {
            const searchInput = document.getElementById('searchInput');
            
            searchInput.addEventListener('input', () => {
                const searchTerm = searchInput.value.toLowerCase();
                const filteredColors = colors.filter(color => 
                    color.name.toLowerCase().includes(searchTerm) ||
                    color.hex.toLowerCase().includes(searchTerm) ||
                    color.rgb.toLowerCase().includes(searchTerm)
                );
                
                renderTable(filteredColors);
            });
        }

        // Inicializar
        document.addEventListener('DOMContentLoaded', () => {
            renderTable(colors);
            setupSearch();
        });
    </script>
</body>
</html>
