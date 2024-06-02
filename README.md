# GITHUB
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FLORICULTURA FERREIRA</title>
    <style>
        .flor {
            border: 1px solid #ccc;
            padding: 10px;
            margin-bottom: 10px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <h1>Escolha suas flores</h1>
    <div class="flor" id="Buque Rosas">
        <h2>Buque Rosas</h2>
        <p>Cor: Vermelho</p>
        <p>Preço: R$ 200.00</p>
        <button onclick="adicionarAoCarrinho('RosaBuque Rosas')">Adicionar ao Carrinho</button>
    </div>
    <div class="flor" id="Buque Girassol mais Rosas">
        <h2>Buque Girassol mais Rosas</h2>
        <p>Cor: Amarelo e Vermelho</p>
        <p>Preço: R$ 150.00</p>
        <button onclick="adicionarAoCarrinho('Buque Girassol mais Rosas')">Adicionar ao Carrinho</button>
    </div>
    <div class="flor" id="Buque Girassol">
        <h2>Buque Girassol</h2>
        <p>Cor: Amarelo</p>
        <p>Preço: R$ 100.00</p>
        <button onclick="adicionarAoCarrinho('Buque Girassol')">Adicionar ao Carrinho</button>
    </div>
    
    <h2>Carrinho de Compras</h2>
    <ul id="carrinho">
    </ul>

    <script>
        let carrinho = [];

        function adicionarAoCarrinho(nomeFlor) {
            carrinho.push(nomeFlor);
            atualizarCarrinho();
        }

        function atualizarCarrinho() {
            const carrinhoElemento = document.getElementById('carrinho');
            carrinhoElemento.innerHTML = '';
            carrinho.forEach((item) => {
                const li = document.createElement('li');
                li.textContent = item;
                carrinhoElemento.appendChild(li);
            });
        }
    </script>
</body>
</html>
