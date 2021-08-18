---
description: In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per alfa, rosso, verde e blu.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Linee e riempimenti con fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64096bbabc632ad7c2b159191ad21b3b09f3801a486f27679118008e4927e88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977801"
---
# <a name="alpha-blending-lines-and-fills"></a>Linee e riempimenti con fusione alfa

In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per alfa, rosso, verde e blu. Il valore alfa indica la trasparenza del colore, ovvero la misura in cui il colore viene misto con il colore di sfondo. I valori alfa sono da 0 a 255, dove 0 rappresenta un colore completamente trasparente e 255 rappresenta un colore completamente opaco.

La fusione alfa è una fusione pixel per pixel dei dati di origine e dei colori di sfondo. Ognuno dei tre componenti (rosso, verde, blu) di un determinato colore di origine viene misto con il componente corrispondente del colore di sfondo in base alla formula seguente:

displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255

Si supponga, ad esempio, che il componente rosso del colore di origine sia 150 e che il componente rosso del colore di sfondo sia 100. Se il valore alfa è 200, il componente rosso del colore risultante viene calcolato come segue:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

Gli argomenti seguenti descrivono in modo più dettagliato la fusione alfa:

-   [Disegno di linee opache e semitrasparenti](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Disegno con pennelli opachi e semitrasparenti](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Uso della modalità di composizione per controllare la fusione alfa](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Uso di una matrice di colori per impostare valori alfa nelle immagini](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Impostazione dei valori alfa di singoli pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



