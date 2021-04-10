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
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="0645e-103">Note sull'implementazione per le API StylusInput</span><span class="sxs-lookup"><span data-stu-id="0645e-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="0645e-104">Le classi [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))e [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) sono implementate come wrapper com e sono disponibili solo nel codice gestito.</span><span class="sxs-lookup"><span data-stu-id="0645e-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="0645e-105">Quando l'oggetto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) viene aggiunto come plug-in a un oggetto **RealTimeStylus** , gli oggetti COM sottostanti interagiscono a livello com.</span><span class="sxs-lookup"><span data-stu-id="0645e-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="0645e-106">Pertanto, la chiamata diretta dei metodi delle interfacce [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0645e-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="0645e-107">Aggiungere l'oggetto **RealTimeStylus**, GestureRecognizer o DynamicRenderer all'oggetto **RealTimeStylus** è l'unico modo per accedere a queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0645e-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
