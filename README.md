# php-alert
Sistema de alerta de mensagens em PHP e JAVASCRIPT

COLOCA NO HEADER
<link rel="stylesheet" href="ionicons/css/ionicons.min.css"/>    
<link rel="stylesheet" href="toastr/build/toastr.min.css"/>

COLOCA NO JAVASCRIPT
<script type="text/javascript" src="<?=$raiz?>files/plugin/stisla/modules/toastr/build/toastr.min.js"></script>

COLOCA NO TOPO DO ARQUIVO
include($raiz . "Alerta.php");
$alerta         = new Alerta();
$alertaMsgRecebida = $alerta->verificaMsg();

COLOCA NO FINAL DA PÁGINA
<?=$alertaMsgRecebida?>

IMPLEMENTAÇÃO NO PHP
$alerta->warning("texto mensagem", "PAGINA DESTINO");
$alerta->danger("texto mensagem", "PAGINA DESTINO");
$alerta->info("texto mensagem", "PAGINA DESTINO");
$alerta->success("texto mensagem", "PAGINA DESTINO");

IMPLEMENTAÇÃO NO JAVASCRIPT
toastr.error('MENSAGEM', 'TITULO');
toastr.warning('MENSAGEM', 'TITULO');
toastr.error('MENSAGEM', 'TITULO');
toastr.info('MENSAGEM', 'TITULO');
toastr.success('MENSAGEM', 'TITULO');

