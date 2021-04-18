---
description: ATM rientra nella categoria dei dati con radice e dei piani di controllo rooted.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Da punto ATM a MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307052"
---
# <a name="atm-point-to-multipoint"></a>Da punto ATM a MultiPoint

ATM rientra nella categoria dei dati con radice e dei piani di controllo rooted. Un'applicazione che funge da radice creerebbe i \_ socket radice c e le controparti in esecuzione nei nodi foglia utilizzeranno i \_ socket foglia c. L'applicazione radice USA [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere nuovi nodi foglia. Le applicazioni corrispondenti nei nodi foglia avranno impostato i \_ socket foglia c in modalità di ascolto. **WSAJoinLeaf** con un \_ socket radice c specificato viene mappato al messaggio Q. 2931 ADDPARTY. Il join avviato da foglia non è supportato in ATM UNI 3,1, ma è supportato in ATM UNI 4,0. Di conseguenza, **WSAJoinLeaf** con un \_ socket foglia c specificato viene mappato al messaggio ATM UNI 4,0 appropriato.

Ci sono considerazioni aggiuntive da tenere presenti per l'ATM da punto a multipoint:

-   L'aggiunta di nuove foglie alla sessione ATM da punto a MultiPoint è solo basata su invito. La radice invita le foglie, che hanno già la chiamata di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , chiamando la funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Il flusso di dati in una sessione ATM da punto a MultiPoint è da solo da radice a foglia; leaves non può usare la stessa sessione per inviare informazioni alla radice.
-   È consentita una sola foglia per ogni adapter ATM.

 

 



