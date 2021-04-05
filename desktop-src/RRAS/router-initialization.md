---
title: Inizializzazione router
description: Le informazioni di configurazione per il router, i gestori del router e i protocolli/client di routing sono divise in informazioni globali e per informazioni sull'interfaccia e vengono archiviate nel registro di sistema e nel file di rubrica del router, router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- router RRAS, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707048"
---
# <a name="router-initialization"></a>Inizializzazione router

Le informazioni di configurazione per il router, i gestori del router e i protocolli/client di routing sono divise in informazioni globali e per informazioni sull'interfaccia e vengono archiviate nel registro di sistema e nel file di rubrica del router, router. pbk.

All'avvio del processo del router, DIM (Dynamic Interface Manager) legge la configurazione del router dal registro di sistema. DIM crea le interfacce specificate dalle informazioni sull'interfaccia.

DIM consente inoltre di recuperare le informazioni di gestione router globali. DIM avvia le gestioni router corrispondenti a queste informazioni e le passa alle informazioni. Se, ad esempio, DIM trova le informazioni globali per gestione router IP nel registro di sistema, DIM avvia Gestione router IP e le passa alle informazioni globali. Se nel registro di sistema non sono presenti informazioni globali per un determinato gestore di router, DIM non avvia tale gestore di router.

I gestori di router esaminano le informazioni globali ricevute da DIM. Se Gestione router trova informazioni specifiche per un particolare client all'interno delle informazioni globali, gestione router carica la DLL per il client (ad esempio IpNAT.dll) e inizializza il client chiamando le funzioni [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) e [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) del client. Gestione router passa al client le informazioni globali specifiche del client nella chiamata a [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).

In ogni fase, le informazioni passate all'entità successiva sono opache per l'entità che lo precede. Ovvero DIM non interpreta le informazioni globali per gestione router IP, oltre al fatto che le informazioni sono destinate a gestione router IP. Analogamente, gestione router IP non interpreta le informazioni specifiche di OSPF oltre al fatto che si tratta di informazioni OSPF.

 

 




