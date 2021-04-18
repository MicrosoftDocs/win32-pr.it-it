---
title: Identificatore dell'oggetto OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility usa l' \_ identificatore di oggetto QUERYCLASSNAMEIDX di ObjID con il \_ messaggio WM GetObject per determinare la classe a cui appartiene un controllo Windows standard o un controllo comune.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297823"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>\_Identificatore oggetto QUERYCLASSNAMEIDX ObjID

Microsoft Active Accessibility usa l'identificatore di oggetto [**\_ QUERYCLASSNAMEIDX di ObjID**](object-identifiers.md) con il messaggio [**WM \_ GetObject**](wm-getobject.md) per determinare la classe a cui appartiene un controllo Windows standard o un controllo comune. Un controllo risponde a questo messaggio restituendo un valore che Microsoft Active Accessibility esegue il mapping al nome della classe del controllo. Microsoft Active Accessibility utilizza queste informazioni per fornire supporto per l'accessibilità per i controlli Windows standard e i controlli comuni.

Generalmente, solo i controlli Windows standard e i controlli comuni rispondono all'identificatore di oggetto [**\_ QUERYCLASSNAMEIDX di ObjID**](object-identifiers.md) . Tuttavia, un controllo personalizzato può anche rispondere se include tutte le stesse funzionalità di un controllo Windows standard o di un controllo comune esistente. In questo modo il controllo personalizzato sarà supportato da uno degli oggetti proxy standard forniti da Microsoft Active Accessibility.

Per ulteriori informazioni, vedere [Appendice F: valori identificatore oggetto per objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 




