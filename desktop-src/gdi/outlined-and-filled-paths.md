---
description: Un'applicazione può disegnare il contorno di un tracciato chiamando la funzione StrokePath, può riempire l'interno di un tracciato chiamando la funzione FillPath e può sia delineare che riempire il tracciato chiamando la funzione StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Tracciati con contorni e riempiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9660221eb1ef9d7ecf80d1d48ae18c8b234e76e5af3b30dba3323ee6feac3bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831601"
---
# <a name="outlined-and-filled-paths"></a>Tracciati con contorni e riempiti

Un'applicazione può disegnare il contorno di un tracciato chiamando la funzione [**StrokePath,**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) può riempire l'interno di un tracciato chiamando la funzione [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) e può sia delineare che riempire il tracciato chiamando la funzione [**StrokeAndFillPath.**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath)

Ogni volta che un'applicazione riempie un percorso, il sistema usa la modalità di riempimento corrente del controller di dominio. Un'applicazione può recuperare questa modalità chiamando la [**funzione GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) e può impostare una nuova modalità di riempimento chiamando la [**funzione SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) Per una descrizione delle due modalità di riempimento, vedere [Aree](regions.md).

Nella figura seguente viene illustrata la sezione incrociata di un oggetto creato da un'applicazione CAD (Computer-Aided Design) usando percorsi sia delineati che riempiti.

![illustrazione che mostra la visualizzazione sezionata incrociata di un oggetto, con varie parti indicate da modelli di riempimento diversi](images/cspth-01.png)

 

 



