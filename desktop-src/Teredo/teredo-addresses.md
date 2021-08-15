---
title: Teredo Indirizzi
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Altre informazioni su: Teredo indirizzi'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354137"
---
# <a name="teredo-addresses"></a>Teredo Indirizzi

Un Teredo è costituito da quanto segue:

-   **Teredo prefisso**

    I primi 32 bit sono per il prefisso Teredo, che è lo stesso per tutti Teredo indirizzi. Windows XP e Windows Server 2003 usava inizialmente il prefisso 3FFE:831F::/32 Teredo. Il prefisso definito per Teredo in RFC 4380 è 2001::/32 ed è il prefisso usato da Teredo in Windows Vista e Windows Server 2008. I computer che eseguono Windows XP e Windows Server 2003 useranno il prefisso Teredo 2001::/32 quando vengono aggiornati con il Bollettino Microsoft sulla sicurezza MS06-064.

-   **Teredo indirizzo IPv4 del server**

    I 32 bit successivi contengono l'indirizzo pubblico IPv4 del server Teredo che ha contribuito a configurare questo Teredo indirizzo. Per altre informazioni, vedere "Configurazione iniziale per Teredo client" in questo articolo.

-   **Flag**

    I 16 bit successivi per sono riservati per Teredo flag. Per Windows client basati Teredo XP, l'unico flag definito è il bit di ordine elevato noto come flag Cone. Il flag Cone viene impostato quando Teredo client è dietro un NAT cono. La determinazione del fatto che il NAT connesso a Internet sia un NAT cono si verifica durante Teredo configurazione iniziale del client. Per altre informazioni, vedere "Configurazione iniziale per Teredo client" in questo articolo.

    Per Windows client Teredo basati su Windows Vista e Windows Server 2008, i bit inutilizzati all'interno del campo Flag forniscono un livello di protezione dalle analisi degli indirizzi da parte di utenti malintenzionati. I 16 bit nel campo Flag per Windows Vista e i client Teredo basati su Windows Server 2008 sono i seguenti: CRAAAAUG AAAAAAAA. Il bit C è per il flag Cone. Il bit R è riservato per un uso futuro. Il bit U è per il flag Universal/Local (impostato su 0). Il bit G è il flag Individual/Group (impostato su 0). I bit A sono impostati su un numero generato in modo casuale a 12 bit. Usando un numero casuale per i bit A, un utente malintenzionato che ha determinato il resto dell'indirizzo Teredo acquisendo lo scambio di configurazione iniziale dei pacchetti tra il client Teredo e il server Teredo dovrà provare fino a 4.096 (212) indirizzi diversi per determinare l'indirizzo di un client Teredo durante un'analisi degli indirizzi.

-   **Porta esterna nascosta**

    I 16 bit successivi archiviano una versione nascosta della porta UDP esterna corrispondente a tutto Teredo traffico per questo Teredo client. Quando il client Teredo invia il pacchetto iniziale a un server Teredo, la porta UDP di origine del pacchetto viene mappata dal NAT a una porta UDP esterna diversa. Il Teredo client mantiene questo mapping delle porte in modo che rimanga nella tabella di conversione del NAT. Pertanto, tutto Teredo traffico per l'host usa la stessa porta UDP esterna mappata. La porta UDP esterna è determinata dal server Teredo dalla porta UDP di origine del pacchetto iniziale in ingresso inviato dal client Teredo e inviato nuovamente al client Teredo.

    La porta esterna viene nascosta da XORing la porta esterna con 0xFFFF. Ad esempio, la versione nascosta della porta esterna 5000 in formato esadecimale è EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). L'oscuramento della porta esterna impedisce ai NAT di tradurre la porta esterna all'interno del payload dei pacchetti che inoltrano.

-   **Indirizzo esterno nascosto**

    Gli ultimi 32 bit archiviano una versione nascosta dell'indirizzo IPv4 esterno corrispondente a tutto Teredo traffico per questo Teredo client. Proprio come la porta esterna, quando il client Teredo invia il pacchetto iniziale a un server Teredo, l'indirizzo IP di origine del pacchetto viene mappato dal NAT a un indirizzo esterno (pubblico) diverso. Il Teredo client mantiene questo mapping degli indirizzi in modo che rimanga nella tabella di conversione del NAT. Pertanto, tutto Teredo traffico per l'host usa lo stesso indirizzo IPv4 esterno, mappato e pubblico. L'indirizzo IPv4 esterno è determinato dal server Teredo dall'indirizzo IPv4 di origine del pacchetto iniziale in ingresso inviato dal client Teredo e inviato nuovamente al client Teredo.

    L'indirizzo esterno viene nascosto da XORing l'indirizzo esterno con 0xFFFFFFFF. Ad esempio, la versione nascosta dell'indirizzo IPv4 pubblico 131.107.0.1 in formato esadecimale due punti è 7C94:FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). L'obscuring dell'indirizzo esterno impedisce ai NAT di tradurre l'indirizzo esterno all'interno del payload dei pacchetti che inoltrano.

 

 




