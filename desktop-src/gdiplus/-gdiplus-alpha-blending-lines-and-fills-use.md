---
description: In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per Alpha, rosso, verde e blu.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Linee e riempimenti con fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880929"
---
# <a name="alpha-blending-lines-and-fills"></a>Linee e riempimenti con fusione alfa

In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per Alpha, rosso, verde e blu. Il valore alfa indica la trasparenza del colore, ovvero la misura in cui il colore viene mescolato con il colore di sfondo. I valori alfa variano da 0 a 255, dove 0 rappresenta un colore completamente trasparente e 255 rappresenta un colore completamente opaco.

La fusione alfa è una combinazione pixel per pixel dei dati di origine e di colore di sfondo. Ognuno dei tre componenti (rosso, verde, blu) di un determinato colore di origine viene mescolato con il componente corrispondente del colore di sfondo in base alla formula seguente:

displayColor = sourceColor × Alpha/255 + backgroundColor × (255 – Alpha)/255

Si supponga, ad esempio, che il componente rosso del colore di origine sia 150 e che il componente rosso del colore di sfondo sia 100. Se il valore alfa è 200, il componente rosso del colore risultante viene calcolato come segue:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

Gli argomenti seguenti riguardano la fusione alfa in modo più dettagliato:

-   [Disegno di linee opache e semitrasparenti](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Disegno con pennelli opachi e semitrasparenti](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Uso della modalità di composizione per controllare la fusione alfa](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Uso di una matrice di colori per impostare valori alfa nelle immagini](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Impostazione dei valori alfa dei singoli pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



