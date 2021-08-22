---
description: ATM rientra nella categoria dei dati rooted e dei piani di controllo rooted.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM Da punto a multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198d8160fdb1e942cc581374af18ca57303726bdddd41142855d366e58dfbf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504461"
---
# <a name="atm-point-to-multipoint"></a>ATM Da punto a multipunto

ATM rientra nella categoria dei dati rooted e dei piani di controllo rooted. Un'applicazione che funge da radice creerebbe socket radice c e le controparti in esecuzione nei nodi foglia \_ utilizzerebbe socket foglia \_ c. L'applicazione radice [**usa WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere nuovi nodi foglia. Le applicazioni corrispondenti nei nodi foglia avranno impostato i socket foglia c \_ in modalità di ascolto. **WSAJoinLeaf** con un socket radice c specificato viene mappato al messaggio \_ Q.2931 ADDPARTY. L'aggiunta avviata da foglia non è supportata in ATM UNI 3.1, ma è supportata in ATM UNI 4.0. **WSAJoinLeaf** con un socket foglia c specificato viene quindi mappato al \_ messaggio ATM UNI 4.0 appropriato.

Per ATM da punto a multipunto è necessario tenere presenti alcune considerazioni aggiuntive:

-   L'aggiunta di nuove lascia alla sessione da punto a multipunto del bancomat è solo basata su invito. La radice invita a lasciare, che hanno già la chiamata di funzione [**accept,**](/windows/desktop/api/Winsock2/nf-winsock2-accept) chiamando la [**funzione WSAJoinLeaf.**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)
-   Il flusso di dati in una sessione da punto a multipunto atm è solo da root a leaves; Leaves non può usare la stessa sessione per inviare informazioni alla radice.
-   È consentita una sola foglia per ogni adapter ATM.

 

 



