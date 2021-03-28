---
description: Un'applicazione può tracciare il contorno di un percorso chiamando la funzione StrokePath, può riempire l'area interna di un percorso chiamando la funzione FillPath ed è in grado di delineare e riempire il percorso chiamando la funzione StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Percorsi delineati e riempiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967058"
---
# <a name="outlined-and-filled-paths"></a>Percorsi delineati e riempiti

Un'applicazione può tracciare il contorno di un percorso chiamando la funzione [**strokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , può riempire l'area interna di un percorso chiamando la funzione [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) ed è in grado di delineare e riempire il percorso chiamando la funzione [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .

Ogni volta che un'applicazione compila un percorso, il sistema utilizza la modalità di riempimento corrente del controller di dominio. Un'applicazione può recuperare questa modalità chiamando la funzione [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) e può impostare una nuova modalità di riempimento chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Per una descrizione delle due modalità di riempimento, vedere [aree](regions.md).

Nella figura seguente viene illustrata la sezione incrociata di un oggetto creato da un'applicazione di progettazione assistita da computer (CAD) utilizzando percorsi che sono stati entrambi delineati e riempiti.

![illustrazione che mostra la visualizzazione tra sezioni di un oggetto, con varie parti indicate da modelli di riempimento diversi](images/cspth-01.png)

 

 



