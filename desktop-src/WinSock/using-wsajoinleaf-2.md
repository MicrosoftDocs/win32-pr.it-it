---
description: Come accennato in precedenza, la funzione WSAJoinLeaf viene usata per unire un nodo foglia a una sessione multipoint.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Uso di WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13b6d82960f74135fa519a1284a1274b878e18c32f59d9c2b8c46ebd592c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121021"
---
# <a name="using-wsajoinleaf"></a>Uso di WSAJoinLeaf

Come accennato in [**precedenza, la funzione WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usata per unire un nodo foglia a una sessione multipoint. **WSAJoinLeaf** ha gli stessi parametri e la stessa semantica di [**WSAConnect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) ad eccezione del fatto che restituisce un descrittore socket (come in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) e ha un parametro *dwFlags* aggiuntivo.

Il *parametro dwFlags* viene usato per indicare se il socket fungerà solo da mittente, solo come ricevitore o da entrambi. In questa funzione è possibile usare solo socket multipoint per i *parametri di* input. Se il socket multipoint è in modalità non di blocco, il descrittore del socket restituito non è utilizzabile fino a quando non viene ricevuta un'indicazione FD \_ CONNECT corrispondente. Un'applicazione radice in una sessione multipoint può chiamare [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) una o più volte per aggiungere un numero di nodi foglia, ma al massimo una richiesta di connessione multipoint può essere in sospeso alla volta.

Il descrittore del socket restituito da [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) varia a seconda che il descrittore del socket di input, *s*, sia una radice c o una foglia \_ \_ c. Se usato con un socket radice c, il parametro name definisce un nodo foglia specifico da aggiungere e il descrittore del socket restituito è un socket foglia c corrispondente al nodo foglia \_ appena  \_ aggiunto. Non deve essere usato per lo scambio di dati multipunto, ma viene usato per ricevere indicazioni FD \_ XXX (ad esempio, FD CLOSE) per la connessione esistente alla foglia \_ c \_ specifica. Alcune implementazioni multipoint possono anche consentire l'uso di questo socket per le chat laterali tra la radice e un singolo nodo foglia. Viene ricevuta un'indicazione CLOSE FD per questo socket se il nodo foglia corrispondente chiama \_ [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per uscire dalla sessione multipoint. In modo simmetrico, se si richiama **closesocket** sul socket foglia C restituito da \_ **WSAJoinLeaf,** il socket nel nodo foglia corrispondente ottiene una notifica CLOSE FD. \_

Quando [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene richiamato con un socket foglia c, il parametro name contiene l'indirizzo dell'applicazione radice (per uno schema di controllo rooted) o di una sessione multipoint esistente (schema di controllo non rooted) e il descrittore del socket restituito è lo stesso del descrittore \_ del socket di input.  In uno schema di controllo rooted, l'applicazione radice mette il socket radice c in modalità di ascolto \_ chiamando [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). La notifica standard FD \_ ACCEPT viene recapitata quando il nodo foglia richiede di unirsi alla sessione multipoint. L'applicazione radice usa [**le**](/windows/desktop/api/Winsock2/nf-winsock2-accept)normali funzioni / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) accept per accettare il nuovo nodo foglia. Anche il valore restituito da **accept** o **WSAAccept** è un descrittore del socket foglia c esattamente come quelli \_ restituiti da **WSAJoinLeaf.** Per supportare schemi multipoint che consentono sia i join avviati dalla radice che i join foglia, è accettabile che un socket radice c già in modalità di ascolto sia usato come input per \_ **WSAJoinLeaf**.

Un'applicazione radice multipunto è in genere responsabile dell'smantellamento ordinato di una sessione multipoint. Un'applicazione di questo tipo può usare shutdown [**o**](/windows/desktop/api/winsock/nf-winsock-shutdown) [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) in un socket radice c per fare in modo che tutti i socket foglia c associati, inclusi quelli restituiti da \_ \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) e i socket foglia c corrispondenti nei nodi foglia remoti, otterrà la notifica \_ FD \_ CLOSE.

 

 



