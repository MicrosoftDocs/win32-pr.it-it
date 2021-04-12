---
title: Indirizzi Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Altre informazioni su: indirizzi Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc08a53da2f710423d948e9479df2aeb08f20178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349646"
---
# <a name="teredo-addresses"></a>Indirizzi Teredo

Un indirizzo Teredo è costituito dagli elementi seguenti:

-   **Prefisso Teredo**

    I primi 32 bit sono per il prefisso Teredo, che è lo stesso per tutti gli indirizzi Teredo. Windows XP e Windows Server 2003 usavano inizialmente il prefisso 3FFE: 831F::/32 Teredo. Il prefisso definito per Teredo in RFC 4380 è 2001::/32 ed è il prefisso utilizzato da Teredo in Windows Vista e Windows Server 2008. I computer che eseguono Windows XP e Windows Server 2003 utilizzeranno il prefisso Teredo 2001::/32 quando vengono aggiornati con Microsoft Security Bulletin MS06-064.

-   **Indirizzo IPv4 del server Teredo**

    I successivi 32 bit contengono l'indirizzo IPv4 pubblico del server Teredo che ha consentito di configurare questo indirizzo Teredo. Per ulteriori informazioni, vedere "configurazione iniziale per client Teredo" in questo articolo.

-   **Flag**

    I successivi 16 bit per sono riservati ai flag Teredo. Per i client Teredo basati su Windows XP, l'unico flag definito è il bit di ordine superiore noto come flag cono. Il flag cono viene impostato quando il client Teredo è dietro un cono NAT. La determinazione dell'eventuale NAT connesso a Internet è un cono NAT durante la configurazione iniziale del client Teredo. Per ulteriori informazioni, vedere "configurazione iniziale per client Teredo" in questo articolo.

    Per i client Teredo basati su Windows Vista e Windows Server 2008, i bit inutilizzati nel campo Flags forniscono un livello di protezione dalle analisi degli indirizzi da parte di utenti malintenzionati. I 16 bit nel campo flag per i client Teredo basati su Windows Vista e Windows Server 2008 sono costituiti dai seguenti elementi: CRAAAAUG ALABASTR. Il bit C è per il flag conico. Il bit R è riservato per un uso futuro. Il bit U è per il flag universale/locale (impostato su 0). Il bit G è un flag di gruppo/singolo (impostato su 0). I bit a sono impostati su un numero a 12 bit generato in modo casuale. Utilizzando un numero casuale per i bit A, un utente malintenzionato che ha determinato il resto dell'indirizzo Teredo acquisendo lo scambio di configurazione iniziale dei pacchetti tra il client Teredo e il server Teredo dovrà provare fino a 4.096 (212) indirizzi diversi per determinare l'indirizzo di un client Teredo durante un'analisi degli indirizzi.

-   **Porta esterna nascosta**

    I successivi 16 bit archiviano una versione nascosta della porta UDP esterna corrispondente a tutto il traffico Teredo per questo client Teredo. Quando il client Teredo invia il pacchetto iniziale a un server Teredo, la porta UDP di origine del pacchetto viene mappata da NAT a un'altra porta UDP esterna. Il client Teredo gestisce questo mapping delle porte, in modo che rimanga nella tabella di conversione del NAT. Pertanto, tutto il traffico Teredo per l'host utilizza la stessa porta UDP con mapping esterno. La porta UDP esterna è determinata dal server Teredo dalla porta UDP di origine del pacchetto iniziale in ingresso inviato dal client Teredo e restituito al client Teredo.

    La porta esterna è nascosta XOR la porta esterna con 0xFFFF. Ad esempio, la versione nascosta della porta esterna 5000 in formato esadecimale è EC77 (5000 = 0X1388, 0X1388 XOR 0xFFFF = 0xEC77). Se si nasconde la porta esterna, i NAT non possono tradurre la porta esterna all'interno del payload dei pacchetti che stanno inoltrando.

-   **Indirizzo esterno nascosto**

    Gli ultimi 32 bit archiviano una versione nascosta dell'indirizzo IPv4 esterno corrispondente a tutto il traffico Teredo per questo client Teredo. Proprio come la porta esterna, quando il client Teredo invia il pacchetto iniziale a un server Teredo, l'indirizzo IP di origine del pacchetto viene mappato da NAT a un indirizzo esterno (pubblico) diverso. Il client Teredo gestisce questo mapping degli indirizzi, in modo che rimanga nella tabella di conversione del NAT. Pertanto, tutto il traffico Teredo per l'host utilizza lo stesso indirizzo IPv4 esterno, mappato e pubblico. L'indirizzo IPv4 esterno è determinato dal server Teredo dall'indirizzo IPv4 di origine del pacchetto iniziale in ingresso inviato dal client Teredo e restituito al client Teredo.

    L'indirizzo esterno è nascosto da XOR l'indirizzo esterno con 0xFFFFFFFF. Ad esempio, la versione nascosta dell'indirizzo IPv4 pubblico 131.107.0.1 in formato esadecimale con due punti è 7C94: FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). Se si nasconde l'indirizzo esterno, i NAT non potranno convertire l'indirizzo esterno entro il payload dei pacchetti che stanno inoltrando.

 

 




