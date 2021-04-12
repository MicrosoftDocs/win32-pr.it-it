---
description: In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo di Windows Sockets 2, l'ATM rientra nella categoria dei dati radice e dei piani di controllo rooted.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Dettagli della funzione ATM di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130406"
---
# <a name="winsock-atm-function-details"></a>Dettagli della funzione ATM di Winsock

In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo di Windows Sockets 2, l'ATM rientra nella categoria dei dati radice e dei piani di controllo rooted. (Per altre informazioni, vedere la specifica dell'API di Windows Sockets 2, Appendice D). Un'applicazione che funge da radice creerebbe i \_ socket radice c e le controparti in esecuzione nei nodi foglia utilizzeranno i \_ socket foglia c. Per aggiungere nuovi nodi foglia, l'applicazione radice utilizzerà [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) . Le applicazioni corrispondenti nei nodi foglia avranno impostato i \_ socket foglia c nella modalità di ascolto. **WSAJoinLeaf** con un \_ socket radice c specificato verrà mappato al messaggio di installazione Q. 2931 (per la prima foglia) o al messaggio di aggiunta entità (per qualsiasi foglia successiva).

> [!Note]  
> I parametri QoS specificati in **WSAJoinLeaf** per le foglie successive devono essere ignorati in base alla specifica UNI del forum ATM.

 

Il join avviato da foglia non fa parte del bancomat UNI 3,1, ma è supportato in ATM UNI 4,0. Pertanto [](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) \_ , è possibile eseguire il mapping di WSAJoinLeaf con un socket foglia c al messaggio ATM UNI 4,0 appropriato.

Il parametro AAL e la negoziazione B-LLI sono supportati tramite la modifica delle IEs corrispondenti nel parametro *lpSQOS* alla chiamata della funzione Condition specificata in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).

> [!Note]  
> È possibile modificare solo determinati campi in queste due IEs. Per informazioni dettagliate, vedere la specifica UNI del forum ATM Appendice C e Appendice F.

 

 

 



