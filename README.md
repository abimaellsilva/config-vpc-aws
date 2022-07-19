<h1>[TUTORIAL] Criando uma rede com subredes privada e publica na AWS VPC 🌩</h1>
<h2>[RESQUISITOS]</h2>

<ol>
    <li>Ter uma conta na AWS.</li>
</ol>

<h2>[VAMOS PARA PRÁTICA!]</h2>
<p><b>1ª</b> Na aba de pesquisa na parte de cima procure por VPC e clique na primeira opção da pesquisa.</p>
<img height="400" width="700" src="/src/print/1.vpc.png">

<br>
<p><b>2ª</b> depois disso clique na opção <b>Create VPC</b> para criarmos uma nova VPC.</p>
<img height="400" width="700" src="/src/print/2.vpc.png">

<br>
<p><b>3ª</b> Preencha os campos abaixo:</p>
<ol>
    <li>No campo <b>Name tag</b> escolha o nome para sua rede. Para exemplo usarei o nome de VPC001</li>
    <li>Em <b>IPv4 CIDR block</b> deixe marcado a opção IPv4 CIDR manual input</li>
    <li>Em <b>IPv4 CIDR</b> escolha qual será a faixa de ip geral da sua rede, a partir dela será criado as subredes. No exemplo usarei a faixa de IP 10.0.0.0/16 </li>
    <li>Em <b>IPv6 CIDR block</b> como não vamos trabalhar com o ipv6 deixa marcado a opção <b>No IPv6 CIDR block</b></li>
    <li>Em <b>Tenancy</b> deixe como default</b></li>
</ol>
<img height="780" width="780" src="/src/print/3.vpc.png">
<p> Após isso só clicar o botão abaixo de <b>Create VPC</b> para finalizar essa parte.</p>

<br>
<p><b>4ª</b> Na Coluna da esquerda no início clique em <b>Subnets</b>. </p>
<img height="450" width="450" src="/src/print/4.vpc.png">
<p>Na nova pagina aberta no canto direito da tela clique em <b>Create Subnet</b>. </p>
<img height="450" width="450" src="/src/print/5.vpc.png">

<br>
<p><b>5ª</b>Aqui onde estaremos criando nossas subredes. </p>

<p>Em <b>VPC ID</b> selecione a rede que você criou anteriormente (a minha foi a VPC001).</p>
<img height="450" width="830" src="/src/print/6.vpc.png">

<p>Logo abaixo em <b>Subnet settings</b> crie sua primeira subnet:</p>
<ol>
    <li>Em <b>Subnet name</b> crie um nome para sua subrede. Eu coloquei o nome de Subnet-Private-1a onde 1a é para voce lembrar qual zona de disponibilidade encontra-se sua rede.</li>
    <li>Em <b>Availability Zone</b> escolha a zona de disponibilidade onde será criada sua rede. (importante o entendimento de zona de disponibilidades da AWS)</li>
    <li>Em <b>IPv4 CIDR block</b> escolha qual será a faixa de ip da sua subrede. No exemplo usarei a faixa de IP 10.0.10.0/24 para minha subrede privada.</li>
</ol>
<p>Clicando em  <b>Add new subnet</b> você ja cria sua segunda subrede.</p>
<p>Siga as mesma opções acima modificando o nome da subrede, deixe a mesma zona de disponibilidade da anterior, mude a faixa de ip.</p>
<p>Criarei a segunda subnet para minha subrede publica.</p>

<img height="800" width="850" src="/src/print/7.vpc.png">
<img height="800" width="850" src="/src/print/8.vpc.png">

<p> Após isso só clicar o botão abaixo de <b>Create Subnet</b> para finalizar.</p>