---
description: Un pennello modello (o personalizzato) viene creato da una bitmap definita dall'applicazione o da una bitmap indipendente dal dispositivo (DIB). I rettangoli seguenti sono stati disegnati usando pennelli modello diversi.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pennello per pattern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987872"
---
# <a name="pattern-brush"></a>Pennello per pattern

Un pennello modello (o personalizzato) viene creato da una bitmap definita dall'applicazione o da una bitmap indipendente dal dispositivo (DIB). I rettangoli seguenti sono stati disegnati usando pennelli modello diversi.

![illustrazione che mostra tre caselle, ognuna con un modello diverso](images/csbru-05.png)

Per creare un pennello logico, un'applicazione deve prima creare una bitmap. Dopo la creazione della bitmap, l'applicazione può creare il pennello logico chiamando la funzione [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) o [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , fornendo un handle che identifica la bitmap (o DIB). I pennelli visualizzati nell'illustrazione precedente sono stati creati da bitmap monocromatiche. Per una descrizione delle bitmap, delle DIB e delle funzioni che li creano, vedere [bitmap](bitmaps.md).

 

 



