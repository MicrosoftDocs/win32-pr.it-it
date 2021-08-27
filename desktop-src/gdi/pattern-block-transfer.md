---
description: Il nome della funzione PatBlt (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o il motivo) fino a riempire un rettangolo specificato.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Trasferimento di blocchi di modelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecb51cbe12da80ca643e2d520e8ebe25c4c9fe03d56a8a16e0c55caf5f1ce10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092931"
---
# <a name="pattern-block-transfer"></a>Trasferimento di blocchi di modelli

Il nome della funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o il motivo) fino a riempire un rettangolo specificato. Tuttavia, la funzione è in realtà molto più potente. Prima di replicare il pennello, combina i dati di colore per il motivo con i dati di colore per i pixel esistenti sullo schermo del video usando un'operazione raster (RICE). Un SIMILAR è un'operazione bit per bit che viene applicata ai bit dei dati di colore per il pennello replicato e ai bit di dati di colore per il rettangolo di destinazione nel dispositivo di visualizzazione. Sono presenti 256 ROP. Tuttavia, la **funzione PatBlt** riconosce solo quelle che richiedono un modello e una destinazione (non quelle che richiedono un'origine). La tabella seguente identifica i ROP più comuni.



| Rop       | Descrizione                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copia il modello nella bitmap di destinazione.                                       |
| PATINVERT | Combina la bitmap di destinazione con il modello usando l'operatore XOR booleano. |
| DSTINVERT | Inverte la bitmap di destinazione.                                                     |
| Oscurità | Converte tutto l'output in zeri binari.                                                   |
| Bianchezza | Converte tutto l'output in file binari.                                                    |



 

Per altre informazioni, vedere [Codici di operazione raster.](raster-operation-codes.md)

 

 



