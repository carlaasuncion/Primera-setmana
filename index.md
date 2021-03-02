## Primera setmana
<p>En aquesta setmana he personalitzat el domini, tambe he creat un server i esic en proces de generar un certificat. Ara mostrare pas a pas el que he anat fent:</p>
<h5>Personalitzaci&oacute; del domini.</h5>
<p><img src="https://img.icons8.com/android/24/000000/domain.png" /></p>
<p>Anem a la web https://demo.poste.io/admin/login on l&rsquo;usuari &eacute;s admin@poste.io i la contrasenya admin. Li donem a &ldquo;domains&rdquo; Dins posem el nostre nom i cognom junt amb .io al final.
  
<p><img src="/images/Capt.png" alt="Cat"></p>
  
Despres entrarem al nostre domini i posarem un correu i amb aquest correu li enviarem un missatge a joan@surfacad.edu Tamb&eacute; enviarem un missatge al nostre compte d&rsquo;institut</p>
<h5>Creaci&oacute; d&rsquo;un server</h5>
<p><img src="https://img.icons8.com/dusk/64/000000/server.png" /></p>
<p>-docker volume create volum_mail_server</p>
<p>-docker run -p 443:443 -e TZ=Europe/Andorra -v volum_mail_server:/data --name "surfmailserver" -h "canvia_aquest_domini_o_se_veiem_lany_vinent.noesbroma" -t analogic/poste.io</p>
<h5>Instalar Docker </h5>
<img src="https://img.icons8.com/color/48/000000/docker.png"/>
<p>-sudo apt-get update</p>
<p>-sudo apt-get install apt-transport-https ca-certificates curl gnupg2 software-properties-common</p>
<p>-curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -</p>
<p>-sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian buster stable"</p>
<p>-sudo apt-get update</p>
<p>-sudo apt-get install docker-ce docker-ce-cli containerd.io</p>
<p>-sudo systemctl status docker</p>
<h5>Generaci&oacute; de certificats de servidor i client.</h5>
<p><img src="https://img.icons8.com/doodle/48/000000/certificate.png" /></p>
<p>-sudo apt-get update</p>
<p>-sudo apt install wget libnss3-tools</p>
<p>-export VER="v1.3.0"</p>
<p>-wget -O mkcert https://github.com/FiloSottile/mkcert/releases/download/${VER}/mkcert-${VER}-linux-amd64</p>
<p>-chmod +x mkcert</p>  
<p>-sudo mv mkcert /usr/local/bin</p> 
<p>Ara cada cop que fem mkcert nomdelcertificat.org es creara un certificat</p>  
<p>De moment porto diverses proves per crear el certificat i nose com fer-ho. 😅</p>
<div class="well">
