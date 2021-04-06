---
description: Descrizione dei modi per migliorare le prestazioni quando si usano le API (Application Programming Interface) di StylusInput.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Considerazioni sulle prestazioni per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759806"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Considerazioni sulle prestazioni per l'API StylusInput

Nell'elenco seguente vengono descritti alcuni modi in cui migliorare le prestazioni delle applicazioni che utilizzano le API StylusInput.

-   Usare la proprietà [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) o [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) per sottoscrivere solo i dati rilevanti per il plug-in. In questo modo si riduce il numero complessivo di chiamate al metodo eseguite dall'oggetto [**RealTimeStylus**](realtimestylus-class.md) , riducendo inoltre la complessità del plug-in. L'oggetto **RealTimeStylus** controlla solo la proprietà DataInterest quando viene collegato il plug-in.
-   Ridurre al minimo la complessità dei plug-in sincroni. Plug-in sincroni generalmente chiamati dal thread dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) e possono contribuire a ritardi nella raccolta di input penna.
-   Prendere in considerazione la possibilità di rendere il plug-in asincrono. Se il plug-in è complesso ed è necessario aggiungere dati personalizzati alla coda dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) , prendere in considerazione l'uso di un modello **RealTimeStylus** a cascata e l'aggiunta del plug-in alla raccolta di plug-in sincrona dell'oggetto **RealTimeStylus** secondario. Per ulteriori informazioni sul modello **RealTimeStylus** a cascata, vedere [il modello di RealTimeStylus a cascata](the-cascaded-realtimestylus-model.md).

 

 
