---
description: 'GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e spline di B&\# 233;spline di zier.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Costruzione e creazione di curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78ebd7ce81099d5b7f483939c0f4b238d1f124357bf6e1863b25fedb7e22f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015221"
---
# <a name="constructing-and-drawing-curves"></a>Costruzione e creazione di curve

GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e spline di Bézier. Un'ellisse è definita dal rettangolo di delimitazione; un arco è una parte di un'ellisse definita da un angolo iniziale e da un angolo di sweep. Una spline cardinale è definita da una matrice di punti e da un parametro di disassociato. La curva passa senza problemi attraverso ogni punto della matrice e il parametro della curva influenza il modo in cui la curva si curva. Una spline di Bézier è definita da due punti finali e due punti di controllo: la curva non passa attraverso i punti di controllo, ma i punti di controllo influenzano la direzione e la curva mentre la curva passa da un punto finale all'altro.

Gli argomenti seguenti descrivono le spline di cardinalità e le spline di Bézier in modo più dettagliato:

-   [Disegno di spline cardinali](-gdiplus-drawing-cardinal-splines-use.md)
-   [Disegno di spline di Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



