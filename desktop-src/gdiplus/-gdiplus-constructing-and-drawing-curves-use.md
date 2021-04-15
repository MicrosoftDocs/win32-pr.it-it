---
description: 'GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e B&\# 233; Zier spline.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Costruzione e creazione di curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994309"
---
# <a name="constructing-and-drawing-curves"></a>Costruzione e creazione di curve

GDI+ supporta diversi tipi di curve: ellissi, archi, spline cardinali e spline di Bézier. Un'ellisse è definita dal relativo rettangolo di delimitazione; un arco è una parte di un'ellisse definita da un angolo iniziale e da un angolo di sweep. Una spline di tipo Cardinal viene definita da una matrice di punti e da un parametro di tensionamento, ovvero la curva passa in modo graduale attraverso ogni punto della matrice e il parametro di tensione influenza la curva. Una spline di Bézier è definita da due punti finali e due punti di controllo: la curva non passa attraverso i punti di controllo, ma i punti di controllo influenzano la direzione e la curva quando la curva passa da un punto finale all'altro.

Gli argomenti seguenti illustrano le spline cardinali e le spline di Bézier in modo più dettagliato:

-   [Disegno di spline di cardinalità](-gdiplus-drawing-cardinal-splines-use.md)
-   [Disegno di spline Bézier](-gdiplus-drawing-bezier-splines-use.md)

 

 



