<!DOCTYPE html> 
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Meu Blog</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
</head>
<body>

<!-- Alerta de boas-vindas -->
<div class="alert alert-primary text-center" role="alert">
    Bem-vindo ao meu blog!
</div>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <a class="navbar-brand" href="#">Blog do João</a>
    <div class="collapse navbar-collapse">
        <ul class="navbar-nav ml-auto">
            <li class="nav-item"><a class="nav-link" href="#">Início</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Sobre</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Contato</a></li>
        </ul>
    </div>
</nav>

<div class="container mt-4">
    <div class="row">

        <!-- Conteúdo principal -->
        <div class="col-md-8">
            <?php
            $posts = [
                ["titulo" => "Primeiro Post", "data" => "26/06/2025", "img" => "https://via.placeholder.com/600x200", "texto" => "Este é o conteúdo do primeiro post."],
                ["titulo" => "Segundo Post", "data" => "25/06/2025", "img" => "https://via.placeholder.com/600x200", "texto" => "Este é o conteúdo do segundo post."],
                ["titulo" => "Terceiro Post", "data" => "24/06/2025", "img" => "https://via.placeholder.com/600x200", "texto" => "Este é o conteúdo do terceiro post."]
            ];

            foreach ($posts as $post) {
                echo '
                <div class="card mb-4">
                    <img src="'.$post["img"].'" class="card-img-top">
                    <div class="card-body">
                        <h5 class="card-title">'.$post["titulo"].'</h5>
                        <p class="card-text"><small class="text-muted">'.$post["data"].'</small></p>
                        <p>'.$post["texto"].'</p>
                        <a href="#" class="btn btn-primary">Leia mais...</a>
                    </div>
                </div>';
            }
            ?>
        </div>

        <!-- Sidebar -->
        <div class="col-md-4">
            <div class="card">
                <div class="card-header bg-secondary text-white">Sobre o Autor</div>
                <div class="card-body">
                    <p>Olá! Meu nome é João e sou apaixonado por tecnologia e café. Escrevo sobre tudo um pouco.</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Rodapé com formulário -->
    <footer class="mt-4 p-4 bg-light">
        <h5>Entre em contato</h5>
        <form>
            <div class="form-group">
                <input type="text" class="form-control" placeholder="Nome">
            </div>
            <div class="form-group">
                <input type="email" class="form-control" placeholder="E-mail">
            </div>
            <div class="form-group">
                <textarea class="form-control" placeholder="Mensagem"></textarea>
            </div>
            <button type="submit" class="btn btn-secondary">Enviar</button>
        </form>
        <p class="mt-3">Contato: contato@meublog.com.br | (99) 99999-9999</p>
    </footer>
</div>

</body>
</html>
