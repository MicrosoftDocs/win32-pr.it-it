---
description: Questa configurazione crea un'associazione di sicurezza IPsec (SA) tra due host nella stessa subnet per eseguire l'autenticazione usando l'intestazione di autenticazione (AH) e l'algoritmo di hashing Message Digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configurazione 3: uso di IPsec tra due host con collegamento locale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129215"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configurazione 3: uso di IPsec tra due host con collegamento locale

Questa configurazione crea un'associazione di sicurezza IPsec (SA) tra due host nella stessa subnet per eseguire l'autenticazione usando l'intestazione di autenticazione (AH) e l'algoritmo di hashing Message Digest 5 (MD5). In questo esempio, la configurazione mostrata protegge tutto il traffico tra due host adiacenti: host 1, con indirizzo locale rispetto al collegamento FE80:: 2AA: FF: FE53: A92C e host 2, con indirizzo locale rispetto al collegamento FE80:: 2AA: FF: FE92: D0F1.

**Per utilizzare IPsec tra due host con collegamento locale**

1.  Nell'host 1 creare i file di associazione di sicurezza (SAD) e dei criteri di sicurezza (SPD) vuoti usando il comando ipsec6 c. In questo esempio il comando Ipsec6.exe è ipsec6 c test. In questo modo vengono creati due file per configurare manualmente le associazioni di sicurezza (test. Sad) e i criteri di sicurezza (test. SPD).
2.  Nell'host 1 modificare il file SPD per aggiungere un criterio di sicurezza che protegga tutto il traffico tra l'host 1 e l'host 2.

    La tabella seguente illustra i criteri di sicurezza aggiunti al file test. SPD prima della prima voce per questo esempio (la prima voce nel file test. SPD non è stata modificata).

    | Nome campo file SPD | Valore di esempio              |
    |---------------------|----------------------------|
    | **Criteri**          | 2                          |
    | **RemoteIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **IndirIPLocale**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocollo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AH**                     |
    | **IPSecMode**       | **TRASPORTO**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direzione**       | **Bidirect**               |
    | **Azione**          | **APPLICARE**                  |
    | **IndiceInterfaccia**  | 0                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questi criteri di sicurezza. Le voci di criteri devono essere inserite in ordine numerico decrescente.

3.  Nell'host 1 modificare il file triste aggiungendo le voci SA per proteggere tutto il traffico tra l'host 1 e l'host 2. È necessario creare due associazioni di sicurezza, una per il traffico nell'host 2 e una per il traffico dall'host 2.

    La tabella seguente illustra la prima voce SA aggiunta al file test. Sad per questo esempio (per il traffico nell'host 2).

    | Nome campo file triste | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **Porta**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **Algaut**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. chiave**               |
    | **Direzione**       | **IN uscita**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questa SA.

    La tabella seguente illustra la seconda voce SA aggiunta al file test. Sad per questo esempio (per il traffico dall'host 2).

    | Nome campo file triste | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **Porta**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **Algaut**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. chiave**               |
    | **Direzione**       | **IN ingresso**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questa SA. Le voci SA devono essere posizionate in ordine numerico decrescente.

4.  Nell'host 1 creare un file di testo contenente una stringa di testo utilizzata per autenticare la firma di accesso condiviso creata con l'host 2. In questo esempio, il file test. Key viene creato con il contenuto "This is a test". È necessario includere le virgolette doppie intorno alla stringa chiave affinché la chiave venga letta dallo strumento ipsec6.

    Microsoft IPv6 Technology Preview supporta solo le chiavi configurate manualmente per l'autenticazione di SAs IPsec. Le chiavi manuali vengono configurate creando file di testo che contengono la stringa di testo della chiave manuale. In questo esempio, la stessa chiave per la firma di accesso condiviso viene usata in entrambe le direzioni. È possibile usare chiavi diverse per la firma di accesso condiviso in ingresso e in uscita creando file di chiave diversi e facendo riferimento a essi con il campo chiave nel file triste.

5.  Nell'host 2 creare file di associazione di sicurezza (SAD) e di criteri di sicurezza (SPD) vuoti usando il comando ipsec6 c. In questo esempio il comando Ipsec6.exe è ipsec6 c test. Vengono creati due file con voci vuote per la configurazione manuale delle associazioni di sicurezza (test. Sad) e dei criteri di sicurezza (test. SPD).

    Per semplificare l'esempio, vengono usati gli stessi nomi di file per i file SAD e SPD nell'host 2. È possibile scegliere di utilizzare nomi di file diversi in ogni host.

6.  Nell'host 2 modificare il file SPD per aggiungere un criterio di sicurezza che protegga tutto il traffico tra host 2 e host 1.

    Nella tabella seguente viene illustrata la voce relativa ai criteri di sicurezza aggiunta prima della prima voce al file test. SPD per questo esempio (la prima voce nel file test. SPD non è stata modificata).

    | Nome campo file SPD | Valore di esempio              |
    |---------------------|----------------------------|
    | **Criteri**          | 2                          |
    | **RemoteIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **IndirIPLocale**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocollo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AH**                     |
    | **IPSecMode**       | **TRASPORTO**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Direzione**       | **Bidirect**               |
    | **Azione**          | **APPLICARE**                  |
    | **IndiceInterfaccia**  | 0                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questi criteri di sicurezza. Le voci di criteri devono essere inserite in ordine numerico decrescente.

7.  Nell'host 2 modificare il file triste aggiungendo le voci SA per proteggere tutto il traffico tra host 2 e host 1. È necessario creare due associazioni di sicurezza, una per il traffico nell'host 1 e una per il traffico dall'host 1.

    La tabella seguente illustra il primo SA aggiunto al file test. Sad per questo esempio (per il traffico dall'host 1).

    | Nome campo file triste | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **Porta**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **Algaut**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. chiave**               |
    | **Direzione**       | **IN ingresso**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questa SA.

    La tabella seguente illustra la seconda voce SA aggiunta al file test. Sad per questo esempio (per il traffico nell'host 1).

    | Nome campo file triste | Valore di esempio              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **DestIPAddr**      | **CRITERI**                 |
    | **SrcIPAddr**       | **CRITERI**                 |
    | **Protocollo**        | **CRITERI**                 |
    | **Porta**        | **CRITERI**                 |
    | **SrcPort**         | **CRITERI**                 |
    | **Algaut**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test. chiave**               |
    | **Direzione**       | **IN uscita**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Posizionare un punto e virgola alla fine della riga configurazione di questa SA. Le voci SA devono essere posizionate in ordine numerico decrescente.

8.  Nell'host 2 creare un file di testo contenente una stringa di testo usata per autenticare la firma di accesso condiviso creata con l'host 1. In questo esempio, il file test. Key viene creato con il contenuto "This is a test". È necessario includere le virgolette doppie intorno alla stringa chiave affinché la chiave venga letta dallo strumento ipsec6.
9.  Nell'host 1 aggiungere i criteri di sicurezza e la firma di accesso condiviso configurati dai file SPD e SAD usando il comando ipsec6 a. In questo esempio, ipsec6 viene eseguito un comando di test sull'host 1.
10. Nell'host 2 aggiungere i criteri di sicurezza e la firma di accesso condiviso configurati dai file SPD e SAD usando il comando ipsec6 a. In questo esempio, il ipsec6 un comando di test viene eseguito sull'host 2.
11. Eseguire il ping dell'host 1 dall'host 2 con il comando ping6.

    Se si acquisisce il traffico utilizzando Microsoft Network Monitor o un altro sniffer di pacchetti, verrà visualizzato lo scambio dei messaggi di richiesta echo e risposta echo ICMPv6 con un'intestazione di autenticazione tra l'intestazione IPv6 e l'intestazione ICMPv6.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazioni consigliate per IPv6](recommended-configurations-2.md)
</dt> <dt>

[Singola subnet con indirizzi locali rispetto al collegamento](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Traffico IPv6 tra nodi in subnet diverse di un Internet (6to4) IPv4](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



