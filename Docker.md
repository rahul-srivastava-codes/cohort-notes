<h3>What is docker?</h3>
<p>Docker ek dabba (container) hai jisme app aur uski sari zarurat ki cheezein hoti hain.
Isse app ko install karne ya chalane me dikkat nahi hoti,
aur "mera system me chal raha, uske me nahi" waali problem nahi aati.</p>

<h3>How to install docker</h3>
Google it how to install and to check it is installed or not , open command prompt and type "docker"
if no error you get. Congrats you have installed it
Also try typing "docker run hello-world" in terminal.

<h3>Container</h3>
<p> Container ek virtual dabba hai jisme application aur uski sari zarurat ki cheezein hoti hain,
jisse app bina kisi dikkat ke kisi bhi system par chale — bina "ye file missing hai",
"library nahi hai" waali problem ke.</p>
Maan lo tumne ek Python app banaya jo numpy aur pandas use karta hai. Agar kisi aur system me
numpy install nahi hoga to wo app crash karega.
Lekin agar tum us app ko Docker container me daal do, to wo container ke andar hi numpy,
pandas, Python sab kuch install hota hai. Ab wo container
kahin bhi chalega bina kisi extra setup ke

Docker Image kya hota hai?

    Docker Image ek blueprint (design) hoti hai — jisme bataya gaya hota hai ki container ko kaise banana hai.
    Ye image me app ka code, libraries, dependencies, OS settings — sab kuch hota hai.

📦 Jaise ek cake ka recipe (image) hai — us recipe se tum jitne marzi cake (container) bana sakte ho.
📦 Docker Container kya hota hai?

    Docker Container ek live, running instance hota hai us image ka.
    Ye real me chal raha hota hai — ji

To run any image just do this
docker run <image_name>

port mappping 
docker run -p 3000: 27017 mongo(any command coming on port 3000 shift to 27017 port bro)

run in detached mode
docker run -d -p 3000: 27017 mongo

docker ps -< shows images which are running

docker kill -> kills container or stop it
<h3>Docker engine</h3>
<p>Docker Engine ek software hai jo aapko containers banane, chalane aur manage karne ki suvidha deta hai. Ye ek client-server architecture par kaam karta hai</p>


<h3>What is docker file</h3>
Text document that contains all the commands a user could call on the command line to create an image.

Create a docker file using
from , workdir, expose , cmd, run and etc
later use "docker build -t your-image-name ." to make the image

It is better to inject to environment variable during runtime 


<h2>Layers in docker</h2>
Dockerfile में जो भी instructions likhte ho (jaise FROM, COPY, RUN, etc), unme se har ek instruction ek naya layer banata hai. Ye layers milke ek complete image banate hain.

 Layers ke Fayde:

    Caching: Agar tum Dockerfile me kuch badalte nahi ho, to Docker purani layer ko reuse kar leta hai, jisse build fast hota hai.

    Efficiency: Sirf jo badalte ho wahi rebuild hota hai.

    Storage: Har layer ek tarah ka snapshot hota hai, aur Docker smartly storage manage karta hai.
