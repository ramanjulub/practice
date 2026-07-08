pipeline {
    agent any
    environment {
        DOCKER_IMAGE = "ramanjulu421/nginx-test:latest"   // your Docker Hub ID + repo name
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ramanjulub/practice.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE .'
            }
        }
        stage('Push to Registry') {
            steps {
                sh 'docker push $DOCKER_IMAGE'
            }
        }
        stage('Deploy to Minikube') {
            steps {
                sshagent(['MIIG4wIBAAKCAYEAu06zkOVwlo7uSegC8uXlVOhlHeEBY2L7PZDA0sMK8CBQD4Ie
XtkjpY7oGU0UjN/Y3SA45cm+al+5/sjInmzaaoUzBZBQYzdfm5wRvPLZuSWawwU/
N0ZFb0ajO7oSpK3yUafYLyJuh85LEbx/7Y7HG7rWIQB4XStKDoahyYt841gaknDn
DECxPKXocm0mkv3BiwjwSW7Vi8b53XKFPNHgz0EUJGtU1u1zwCqqLlws3U9CiEm3
fi9Vpg8aBKPcX11b22VPHErqlq0FW4izvnHbZXbmqd/7e47Dp3bBPj4aS56Ca5SE
7A6y0GSW9+KPnQE7f5iVyMU4C1LBimuFiV7PUky6z8Ps1VtncTFpFQg8wTe/i+aK
epbdgDVJV3Zf4G7dtbdwb03gbOKb/1xhMhK8ayksgSc85D6f2lu6Dc3e//VpGdWA
5b1QCePZrssxznxl88NBvECHbogMccacYjLgR78o3+ZY+DBIwKaaZEULcaZAISzy
xlRgCC0RSp+SN/X5AgMBAAECggGAI0BGjyh/LfasZgBiPbCCnp42GY91IW1Jd2a8
w22tq0+JgcGtUZBwIwJoMArPqUufls4vpx921LI7YPYMu7QkzxNObOeiGWocdj7D
H9pcm3m2TKm6If75pl2W7vCv/Yo3JqL+DrDeOHTcr/PX56+NTWy2S/O4s2AoSd+Q
p0u3L1ovdgwFj8rFEHLw8kgUkGlteWsvPcK8Mdg6wjCBXtbpBlhrIAeLKf/6Xtoo
uRzj3KrEDL5C6F6kMeJ5tRHZsaDyDBy4p3if5CRukIIy3jfHCJjIQib6Y3x/y8Wf
bQPREfOOS5bqFSFQhefTCBDz66AQANHakJ6ueKNUYnJ1X3N+9+XiCGUrQH1Lixfk
j8OJjr7SOw47KqSZ60OzcCZX1/MGoIXsda1sdc7lxE4Dm1AGahjBCcSpyg44CF2W
uH0adrJzmFFgqzxpIRKj79wX/5Rla3rSsCGzYO3igx/IaQjJUKft2srAwoAD5OZ6
M97KmssfymW4phVLOfnzcfCLaV35AoHBAOkY0c604uhvDNdU/RqBZhiz5lUm9dpe
sIuF3msFJLGSG/R1f/fVDmjINDBlJtRh5ui/wd0H3FZIcmqVW7F0GlA58YvjsUwe
PdhOre8QEy57Z0sUhgibAgu35vgk/9fgnTfcRuQ4kZ1nnEBtogxERrswxqfgbeLV
MEvL+xnPbMI8b5FgWrfzDVDoHc/BHB31w14G3sHT+pc1vGVyt6e5LiocgiJ+GSVk
bbmgX2c9/6t//CJiYssA6w+l2UorotcnewKBwQDNth6nQ+8XDSOLSNsJgQQXQezN
Hwujnlft4CHTch5e4cNYAQ4V5z/hcHKOSaUhCq+wK/zXVO9LO2/sQxe/Ezaebb0j
WP8FDkELAwiy0KhiXgLIt/w1N1TLlpvJF9c0yeRDUFQEgZD+0Q+JYzqoXfhHgPJF
QOxWzOUay2AD5XpsR3oT1Q+qwhNJMsHBZlNhz/b62jAwq9LQ5w8lJTP0211R30nn
3FL5wmIAyjlHemVdLFBqxa8T5uC1LCewqx30pBsCgcEAzQYTpKjd3Guw88XBSgr+
7kNuGP/Hx2b6Cf6Zf7BqcfV9uSuQf0BbCDbwEJEn8i6al6XysqMzXoEigjUVDaR9
cItGtjBzxevjodqyik+tT3kjhZprui39Qqli8mg40Hy0TGnnwN0w1y5G9TR5ECkN
vaBNW2O/w4CYllK4bh9QHhhiWZBSuvGBiORhNFc6j++XA6EvVXVKOK3/I4wfldr/
i/K/U+9t1sHa8SbqQzj5JLPR5bx8AOqx1nWeBesTtAL5AoHAdlQmOczoAPh706jq
5gKimcZAMpWDGnEA30In8vsX4Tg4J60jrxHAOyt1mcdfByygdtQ2sp6Wr03XSa4m
QLEKoAM74tNUjlHutCjgngtMcJjnPRIoL2xOiHVv0zK1hhYECXxxd84X25viNgMw
QJ0dLfRMZ+26hQuDVfBaoKMl0pci77mFM5JDib16mocDu6XmydEsGzMbJzNiENnf
kx+EBI5OcuLXj/dybEXmwOj02a2d7G0eEnKiG1T017j2mDy1AoHAShHHgnkwAD03
FcoJpdpXbPL18XCfs+njXJXCuIYANPF2o9VO903NlRRlAkd5nc8bjRIbsht8YMzr
G6FdxmMzo7A8hMsUF1nBZd78g3v7hf1W8NKTlquyPPEDvX4q6pwDaQd4nN+/Okdw
jWVnvrcmadD9NBUb1nhxjw41Lh25xlwV+44rFLUiQmfQ8N276Jc11BLQ9+AQq1Df
AwpQ3x6JmrDkQ6CVBD66cGAv5Brtqr9ZBDZT19Uw4iuogTxMRlG/']) {
                    sh '''
                    scp deployment.yaml service.yaml azureuser@VM2_IP:/home/azureuser/k8s-manifests/
                    ssh azureuser@135.235.218.198 "kubectl apply -f ~/k8s-manifests/deployment.yaml && kubectl apply -f ~/k8s-manifests/service.yaml"
                    '''
                }
            }
        }
    }
}
