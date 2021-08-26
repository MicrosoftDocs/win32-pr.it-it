---
description: Questa configurazione crea un'associazione di sicurezza IPsec tra due host nella stessa subnet per eseguire l'autenticazione usando l'intestazione di autenticazione (AH) e l'algoritmo hash Message Digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configurazione 3: uso di IPsec tra due host di collegamento locale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b72485db34e8ff2c4e29a201df258dfb9d2ab9a00717ab515cda982e7ea867dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121431"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configurazione 3: uso di IPsec tra due host di collegamento locale

Questa configurazione crea un'associazione di sicurezza IPsec tra due host nella stessa subnet per eseguire l'autenticazione usando l'intestazione di autenticazione (AH) e l'algoritmo hash Message Digest 5 (MD5). In questo esempio, la configurazione illustrata protegge tutto il traffico tra due host adiacenti: Host 1, con indirizzo locale del collegamento FE80::2AA:FF:FE53:A92C e Host 2, con l'indirizzo locale del collegamento FE80::2AA:FF:FE92:D0F1.

**Per usare IPsec tra due host di collegamento locale**

1.  Nell'Host 1 creare file di associazione di sicurezza (SAD) e criteri di sicurezza (SPD) vuoti usando il comando ipsec6 c. In questo esempio, il Ipsec6.exe comando è ipsec6 c test. Vengono creati due file per configurare manualmente le associazioni di sicurezza (Test.sad) e i criteri di sicurezza (Test.spd).
2.  Nell'Host 1 modificare il file SPD per aggiungere un criterio di sicurezza che protegge tutto il traffico tra Host 1 e Host 2.

    La tabella seguente illustra i criteri di sicurezza aggiunti al file Test.spd prima della prima voce per questo esempio (la prima voce nel file Test.spd non è stata modificata).

    | Nome del campo del file SPD | Valore di esempio              |
    |---------------------|----------------------------|
    | **Criteri**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **Remoteport**      | \*                         |
    | **Protocollo**        | \*                         |
    | **Localport**       | \*                         |
    | **IPSecProtocol**   | **Ah**                     |
    | **IPSecMode**       | **Trasporto**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direzione**       | **BIDIRECT**               |
    | **Azione**          | **Applicare**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura i criteri di sicurezza. Le voci dei criteri devono essere inserite in ordine numerico decrescente.

3.  Nell'Host 1 modificare il file SAD, aggiungendo le voci SA per proteggere tutto il traffico tra l'Host 1 e l'Host 2. È necessario creare due associazioni di sicurezza, una per il traffico verso l'host 2 e una per il traffico dall'Host 2.

    Nella tabella seguente viene illustrata la prima voce sa aggiunta al file Test.sad per questo esempio (per il traffico verso Host 2).

    | Nome del campo del file SAD | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **DestPort**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **Keyfile**         | **Test.key**               |
    | **Direzione**       | **Outbound**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura questa firma di accesso condiviso.

    La tabella seguente illustra la seconda voce sa aggiunta al file Test.sad per questo esempio (per il traffico dall'host 2).

    | Nome del campo del file SAD | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **DestPort**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **Keyfile**         | **Test.key**               |
    | **Direzione**       | **Inbound**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura questa firma di accesso condiviso. Le voci sa devono essere inserite in ordine numerico decrescente.

4.  Nell'Host 1 creare un file di testo contenente una stringa di testo usata per autenticare le SA create con Host 2. In questo esempio il file Test.key viene creato con il contenuto "This is a test". È necessario includere virgolette doppie intorno alla stringa della chiave per consentire la lettura della chiave da parte dello strumento ipsec6.

    Microsoft IPv6 Technology Preview supporta solo chiavi configurate manualmente per l'autenticazione delle SA IPsec. Le chiavi manuali vengono configurate creando file di testo che contengono la stringa di testo della chiave manuale. In questo esempio viene usata la stessa chiave per le SA in entrambe le direzioni. È possibile usare chiavi diverse per le sae in ingresso e in uscita creando file di chiave diversi e facendo riferimento a esse con il campo KeyFile nel file SAD.

5.  Nell'host 2 creare file di associazione di sicurezza (SAD) e criteri di sicurezza (SPD) vuoti usando il comando ipsec6 c. In questo esempio, il Ipsec6.exe comando è ipsec6 c test. Vengono creati due file con voci vuote per la configurazione manuale delle associazioni di sicurezza (Test.sad) e dei criteri di sicurezza (Test.spd).

    Per semplificare l'esempio, nell'host 2 vengono usati gli stessi nomi di file per i file SAD e SPD. È possibile scegliere di usare nomi di file diversi in ogni host.

6.  Nell'host 2 modificare il file SPD per aggiungere un criterio di sicurezza che protegge tutto il traffico tra Host 2 e Host 1.

    Nella tabella seguente viene illustrata la voce dei criteri di sicurezza aggiunta prima della prima voce al file Test.spd per questo esempio (la prima voce nel file Test.spd non è stata modificata).

    | Nome del campo del file SPD | Valore di esempio              |
    |---------------------|----------------------------|
    | **Criteri**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **LocalIPAddr**     | \*                         |
    | **Remoteport**      | \*                         |
    | **Protocollo**        | \*                         |
    | **Localport**       | \*                         |
    | **IPSecProtocol**   | **Ah**                     |
    | **IPSecMode**       | **Trasporto**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direzione**       | **BIDIRECT**               |
    | **Azione**          | **Applicare**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura i criteri di sicurezza. Le voci dei criteri devono essere inserite in ordine numerico decrescente.

7.  Nell'Host 2 modificare il file SAD, aggiungendo le voci SA per proteggere tutto il traffico tra l'Host 2 e l'Host 1. È necessario creare due associazioni di sicurezza: una per il traffico verso l'Host 1 e una per il traffico dall'Host 1.

    La tabella seguente illustra la prima firma di accesso condiviso aggiunta al file Test.sad per questo esempio (per il traffico dall'host 1).

    | Nome del campo del file SAD | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **DestPort**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **Keyfile**         | **Test.key**               |
    | **Direzione**       | **Inbound**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura questa firma di accesso condiviso.

    La tabella seguente illustra la seconda voce sa aggiunta al file Test.sad per questo esempio (per il traffico verso l'Host 1).

    | Nome del campo del file SAD | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **DestPort**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **Keyfile**         | **Test.key**               |
    | **Direzione**       | **Outbound**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Inserire un punto e virgola alla fine della riga che configura questa firma di accesso condiviso. Le voci sa devono essere inserite in ordine numerico decrescente.

8.  Nell'host 2 creare un file di testo contenente una stringa di testo usata per autenticare le SA create con Host 1. In questo esempio il file Test.key viene creato con il contenuto "This is a test". È necessario includere virgolette doppie intorno alla stringa della chiave per consentire la lettura della chiave da parte dello strumento ipsec6.
9.  Nell'host 1 aggiungere i criteri di sicurezza configurati e le SA dai file SPD e SAD usando il comando ipsec6 a. In questo esempio il comando ipsec6 a test viene eseguito nell'host 1.
10. Nell'host 2 aggiungere i criteri di sicurezza configurati e le SA dai file SPD e SAD usando il comando ipsec6. In questo esempio il comando ipsec6 a test viene eseguito nell'host 2.
11. Ping Host 1 da Host 2 con il comando ping6.

    Se si acquisisce il traffico usando Microsoft Network Monitor o un altro sniffer di pacchetti, si dovrebbe vedere lo scambio di messaggi ICMPv6 Echo Request e Echo Reply con un'intestazione di autenticazione tra l'intestazione IPv6 e l'intestazione ICMPv6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> <dt>

[Subnet singola con indirizzi locali di collegamento](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Traffico IPv6 tra nodi in subnet diverse di internetwork IPv4 (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



