# Telefone-
ATELEFONE
// Abrir um aplicativo
function abrirApp(id) {
  document.querySelectorAll('.tela').forEach(tela => {
    tela.style.display = 'none';
  });

  const app = document.getElementById(id);
  if (app) app.style.display = 'block';
}

// Voltar para a tela inicial
function voltarInicio() {
  document.querySelectorAll('.tela').forEach(tela => {
    tela.style.display = 'none';
  });

  document.getElementById('inicio').style.display = 'block';
}

// Bloquear o celular
function bloquearCelular() {
  document.getElementById('inicio').style.display = 'none';
  document.getElementById('bloqueio').style.display = 'block';
}

// Conferir a senha
function conferirSenha(senhaDigitada) {
  if (senhaDigitada === '4826') {
    document.getElementById('bloqueio').style.display = 'none';
    document.getElementById('inicio').style.display = 'block';
    return true;
  }

  return false;
}

// Reiniciar o capítulo
function reiniciarCapitulo() {
  localStorage.removeItem('ametista_mensagens');
  localStorage.removeItem('ametista_capitulo');
  location.reload();
}
