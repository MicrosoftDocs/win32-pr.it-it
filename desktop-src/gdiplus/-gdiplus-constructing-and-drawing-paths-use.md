---
description: Un percorso è una sequenza di primitive grafiche (linee, rettangoli, curve, testo e simili) che possono essere modificate e disegnate come una singola unità. Un percorso può essere suddiviso in figure aperte o chiuse. Una figura può contenere diverse primitive.
ms.assetid: dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4
title: Costruzione e creazione di percorsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe5f1528e58e3df19afbc83bb6acfdc2a6fca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994304"
---
# <a name="constructing-and-drawing-paths"></a>Costruzione e creazione di percorsi

Un percorso è una sequenza di primitive grafiche (linee, rettangoli, curve, testo e simili) che possono essere modificate e disegnate come una singola unità. Un percorso può essere suddiviso in *figure* aperte o chiuse. Una figura può contenere diverse primitive.

È possibile creare un tracciato chiamando il metodo [**Graphics::D rawpath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ed è possibile riempire un percorso chiamando il metodo [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) della classe **Graphics** .

Gli argomenti seguenti riguardano i percorsi in modo più dettagliato:

-   [Creazione di figure da linee, curve e forme](-gdiplus-creating-figures-from-lines-curves-and-shapes-use.md)
-   [Riempimento di figure aperte](-gdiplus-filling-open-figures-use.md)

 

 



