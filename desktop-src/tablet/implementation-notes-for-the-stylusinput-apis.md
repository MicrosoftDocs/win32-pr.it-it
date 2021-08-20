---
description: Le classi RealTimeStylus, GestureRecognizer e DynamicRenderer vengono implementate come wrapper COM e sono disponibili solo nel codice gestito.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Note sull'implementazione per le API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032379"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Note sull'implementazione per le API StylusInput

Le [**classi RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))e [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) vengono implementate come wrapper COM e sono disponibili solo nel codice gestito.

Quando l'oggetto [**RealTimeStylus,**](realtimestylus-class.md) [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) viene aggiunto come plug-in a un **oggetto RealTimeStylus,** gli oggetti COM sottostanti interagiscono a livello COM. Pertanto, la chiamata diretta dei metodi [delle interfacce IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) non è supportata. **L'aggiunta dell'oggetto RealTimeStylus,** GestureRecognizer o DynamicRenderer all'oggetto **RealTimeStylus** è l'unico modo per accedere a queste funzionalità.

 

 
