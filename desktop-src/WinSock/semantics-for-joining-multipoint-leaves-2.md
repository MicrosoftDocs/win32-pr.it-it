---
description: Nell'esempio seguente viene spesso descritto un socket multipoint definendone il ruolo in uno dei due piani (controllo o dati).
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: Semantica per l'Unione di foglie multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310436"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>Semantica per l'Unione di foglie multipoint

Nell'esempio seguente viene spesso descritto un socket multipoint definendone il ruolo in uno dei due piani (controllo o dati). Si noti che lo stesso socket ha un ruolo nell'altro piano, ma questo non è indicato per tenere i riferimenti brevi. Ad esempio, quando viene creato un riferimento a un " \_ socket radice c", può essere una radice c \_ /d \_ o un \_ socket foglia radice c/d \_ .

Negli schemi del piano di controllo rooted i nuovi nodi foglia vengono aggiunti a una sessione multipoint in uno o in due modi diversi. Nel primo metodo, la radice USA [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per avviare una connessione con un nodo foglia e invitarla a diventare un partecipante. Sul nodo foglia, l'applicazione peer deve avere creato un \_ socket foglia c ed essere usato in [**ascolto**](/windows/desktop/api/Winsock2/nf-winsock2-listen) per impostarlo in modalità di ascolto. Il nodo foglia riceve un' \_ indicazione di accettazione FD quando viene invitato per partecipare alla sessione e segnala la volontà di partecipare chiamando [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). L'applicazione radice riceve quindi un' \_ indicazione di connessione FD quando l'operazione di **join** è stata completata.

Nel secondo metodo, i ruoli sono essenzialmente invertiti. L'applicazione radice crea un \_ socket radice c e lo imposta in modalità ascolto. Un nodo foglia che desidera partecipare alla sessione crea un \_ socket foglia c e USA [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per avviare la connessione e richiedere l'ammissione. L'applicazione radice riceve l' \_ accettazione FD quando arriva una richiesta di ammissione in ingresso e ammette il nodo foglia chiamando [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). Il nodo foglia riceve la \_ connessione FD quando è stata accettata.

In un piano di controllo non radice, in cui tutti i nodi sono \_ di foglia c, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usato per avviare l'inclusione di un nodo in una sessione multipoint esistente. \_Quando il join è stato completato e il descrittore di socket restituito è utilizzabile nella sessione MultiPoint, viene fornita un'indicazione di connessione FD. Nel caso del multicast IP, questo corrisponderebbe all'opzione del socket di aggiunta dell'indirizzo IP \_ \_ .

I lettori che hanno familiarità con l'uso del protocollo UDP senza connessione del multicast IP potrebbero essere interessati dalla semantica orientata alla connessione presentata qui. In particolare, la nozione di utilizzo di [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) su un socket UDP e l'attesa di un' \_ indicazione di connessione FD potrebbe essere problematica. Esiste, tuttavia, un ampio precedente per l'applicazione di semantica orientata alla connessione a protocolli senza connessione. È consentita e talvolta utile, ad esempio, per richiamare la funzione di [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect) standard su un socket UDP. Il risultato generale dell'applicazione della semantica orientata alla connessione a socket senza connessione è una restrizione del modo in cui tali socket possono essere utilizzati, anche in questo caso. Un socket UDP usato in **WSAJoinLeaf** avrà alcune restrizioni e in attesa di un'indicazione di \_ connessione FD, che in questo caso indica semplicemente che il messaggio IGMP corrispondente è stato inviato, è una limitazione di questo tipo.

Ci sono pertanto tre istanze in cui un'applicazione utilizzerebbe [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) che funge da:

-   Radice multipoint e invito a una nuova foglia per partecipare alla sessione
-   Foglia che effettua una richiesta di ammissione a una sessione multipoint radice
-   Foglia che cerca l'ammissione a una sessione MultiPoint non radice (ad esempio, multicast IP)

 

 



