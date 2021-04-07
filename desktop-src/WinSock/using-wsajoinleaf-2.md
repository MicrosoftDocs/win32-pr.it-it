---
description: Come indicato in precedenza, la funzione WSAJoinLeaf viene usata per aggiungere un nodo foglia a una sessione multipoint.
ms.assetid: eaa1593a-36eb-4d92-a3d9-91566fc0216b
title: Uso di WSAJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027262a117edc5541a4809481aa4607837343b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882325"
---
# <a name="using-wsajoinleaf"></a>Uso di WSAJoinLeaf

Come indicato in precedenza, la funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usata per aggiungere un nodo foglia a una sessione multipoint. **WSAJoinLeaf** presenta gli stessi parametri e la stessa semantica di [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) , ad eccezione del fatto che restituisce un descrittore di socket (come in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)) ed è dotato di un parametro *dwFlags* aggiuntivo.

Il parametro *dwFlags* viene utilizzato per indicare se il socket fungerà solo da mittente, solo come ricevitore o entrambi. Solo i socket multipoint possono essere utilizzati per *i* parametri di input in questa funzione. Se il socket multipoint è in modalità non di blocco, il descrittore di socket restituito non è utilizzabile fino a quando non \_ viene ricevuta un'indicazione di connessione FD corrispondente. Un'applicazione radice in una sessione MultiPoint può chiamare [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) una o più volte per aggiungere un numero di nodi foglia, ma al massimo una richiesta di connessione multipoint potrebbe essere in attesa alla volta.

Il descrittore di socket restituito da [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) differisce a seconda che il descrittore di socket di input, *s*, sia una \_ radice c o una \_ foglia c. Quando viene usato con un \_ socket radice c, il parametro *Name* designa un particolare nodo foglia da aggiungere e il descrittore di socket restituito è un \_ socket foglia c corrispondente al nodo foglia appena aggiunto. Non è destinato a essere utilizzato per lo scambio di dati MultiPoint, ma viene invece utilizzato per ricevere \_ indicazioni FD xxx, ad esempio FD \_ Close, per la connessione esistente a una particolare foglia c \_ . Alcune implementazioni multipoint possono anche consentire l'uso di questo socket per le chat laterali tra la radice e un singolo nodo foglia. \_Per questo socket viene ricevuta un'indicazione di chiusura FD se il nodo foglia corrispondente chiama [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per uscire dalla sessione multipoint. In modo simmetrico, la chiamata di **chiamata closesocket** sul \_ socket foglia c restituito da **WSAJoinLeaf** fa sì che il socket nel nodo foglia corrispondente ottenga una notifica di \_ chiusura FD.

Quando [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene richiamato con un \_ socket foglia c, il parametro *Name* contiene l'indirizzo dell'applicazione radice (per uno schema di controllo radice) o una sessione multipoint esistente (schema di controllo non radice) e il descrittore di socket restituito è uguale al descrittore di socket di input. In uno schema di controllo rooted, l'applicazione radice inserisce il \_ socket radice c in modalità di ascolto chiamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen). La notifica di \_ accettazione standard FD viene inviata quando il nodo foglia richiede di aggiungersi alla sessione multipoint. L'applicazione radice usa le normali funzioni [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) / [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) per ammettere il nuovo nodo foglia. Il valore restituito da **Accept** o **WSAAccept** è anche un \_ descrittore di socket foglia c analogo a quello restituito da **WSAJoinLeaf**. Per supportare gli schemi multipoint che consentono sia i join avviati dalla radice che quelli avviati da foglia, è accettabile che un \_ socket radice c già in modalità di ascolto venga usato come input per **WSAJoinLeaf**.

Un'applicazione MultiPoint radice è in genere responsabile dello smantellamento ordinato di una sessione multipoint. Un'applicazione di questo tipo può usare [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) o [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) in un socket radice c per fare in modo che \_ tutti i \_ socket foglia c associati, inclusi quelli restituiti da [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) e i socket foglia c corrispondenti \_ nei nodi foglia remoti, per ottenere la \_ notifica di chiusura FD.

 

 



