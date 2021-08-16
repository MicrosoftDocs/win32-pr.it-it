---
description: Descrizione dei modi per migliorare le prestazioni quando si usano le API (Application Programming Interface) StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerazioni sulle prestazioni per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef40ab389687cd42ef516a61f61ab86a7eb79d4efac9ae6e9dd698e93e54bff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856493"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Considerazioni sulle prestazioni per l'API StylusInput

L'elenco seguente descrive alcuni modi per migliorare le prestazioni delle applicazioni che usano le API StylusInput.

-   Usare la [proprietà Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) per sottoscrivere solo i dati rilevanti per il plug-in. In questo modo si riduce il numero complessivo di chiamate al metodo effettuate dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) e si riduce anche la complessità del plug-in. **L'oggetto RealTimeStylus** controlla la proprietà DataInterest solo quando il plug-in è collegato.
-   Ridurre al minimo la complessità dei plug-in sincroni. Plug-in sincroni chiamati in genere dal thread dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e possono contribuire a ritardi nella raccolta dell'input penna.
-   Valutare la possibilità di rendere asincrono il plug-in. Se il plug-in è complesso e deve aggiungere dati personalizzati alla coda dell'oggetto [**RealTimeStylus,**](realtimestylus-class.md) è consigliabile usare un modello **RealTimeStylus** a catena e aggiungere il plug-in alla raccolta sincrona del plug-in dell'oggetto **RealTimeStylus** secondario. Per altre informazioni sul modello **RealTimeStylus** a catena, vedere [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

 

 
