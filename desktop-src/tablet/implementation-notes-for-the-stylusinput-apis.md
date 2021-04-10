---
description: Le classi RealTimeStylus, GestureRecognizer e DynamicRenderer sono implementate come wrapper COM e sono disponibili solo nel codice gestito.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Note sull'implementazione per le API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966517"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Note sull'implementazione per le API StylusInput

Le classi [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))e [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) sono implementate come wrapper com e sono disponibili solo nel codice gestito.

Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) viene aggiunto come plug-in a un oggetto **RealTimeStylus** , gli oggetti COM sottostanti interagiscono a livello com. Pertanto, la chiamata diretta dei metodi delle interfacce [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) non è supportata. Aggiungere l'oggetto **RealTimeStylus**, GestureRecognizer o DynamicRenderer all'oggetto **RealTimeStylus** è l'unico modo per accedere a queste funzionalità.

 

 
