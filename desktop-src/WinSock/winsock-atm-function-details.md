---
description: In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo Windows Sockets 2, il servizio ATM rientra nella categoria dei dati rooted e dei piani di controllo rooted.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Dettagli della funzione ATM di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b089d02653ee996acc249f63144654c952ba724425fb208d9eb35cc9c2589e4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051379"
---
# <a name="winsock-atm-function-details"></a>Dettagli della funzione ATM di Winsock

In base alla tassonomia definita per gli schemi multipoint/multicast indipendenti dal protocollo Windows Sockets 2, il servizio ATM rientra nella categoria dei dati rooted e dei piani di controllo rooted. Per altre informazioni, vedere Windows'API sockets 2, Appendice D. Un'applicazione che funge da radice creerebbe socket radice c e le controparti in esecuzione nei nodi foglia \_ utilizzerebbe socket foglia \_ c. L'applicazione radice userà [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere nuovi nodi foglia. Le applicazioni corrispondenti nei nodi foglia avranno impostato i socket foglia c \_ in modalità di ascolto. **WSAJoinLeaf** con un socket radice c specificato verrà mappato al messaggio Q.2931 SETUP (per la prima foglia) o al messaggio ADD PARTY (per eventuali foglia \_ successive).

> [!Note]  
> I parametri QoS specificati in **WSAJoinLeaf** per eventuali foglia successive devono essere ignorati in base alla specifica UNI del forum ATM.

 

Il join avviato da foglia non fa parte di ATM UNI 3.1, ma è supportato in ATM UNI 4.0. È quindi possibile eseguire il mapping di [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) con un socket foglia c specificato al \_ messaggio ATM UNI 4.0 appropriato.

Il parametro AAL e la negoziazione B-LLI sono supportati tramite la modifica degli IE corrispondenti nel parametro *lpSQOS* alla chiamata della funzione condition specificata in [**WSAAccept.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)

> [!Note]  
> Solo determinati campi in questi due IE possono essere modificati. Per informazioni dettagliate, vedere l'appendice C e l'Appendice F della specifica UNI del forum ATM.

 

 

 



