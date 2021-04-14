---
description: Metafile di Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metafile di Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978626"
---
# <a name="enhanced-format-metafiles"></a>Metafile di Enhanced-Format

Il *metafile di formato migliorato* è costituito dagli elementi seguenti:

-   Un'intestazione
-   Tabella di handle per oggetti GDI
-   Tavolozza privata
-   Matrice di record metafile

I metafile avanzati offrono un'indipendenza reale del dispositivo. È possibile pensare all'immagine archiviata in un metafile migliorato come "snapshot" della visualizzazione video eseguita in un determinato momento. Questo "snapshot" mantiene le dimensioni indipendentemente da dove viene visualizzato in una stampante, un plotter, il desktop o nell'area client di qualsiasi applicazione.

È possibile utilizzare i metafile avanzati per archiviare un'immagine creata utilizzando le funzioni GDI, incluse le nuove funzioni di percorso e trasformazione. Poiché il formato metafile avanzato è standardizzato, le immagini archiviate in questo formato possono essere copiate da un'applicazione a un'altra. Poiché le immagini sono realmente indipendenti dal dispositivo, è garantito che mantengano la loro forma e proporzione su qualsiasi dispositivo di output.

-   [Record metafile avanzati](enhanced-metafile-records.md)
-   [Creazione di metafile migliorata](enhanced-metafile-creation.md)
-   [Operazioni di Metafile avanzate](enhanced-metafile-operations.md)

 

 



