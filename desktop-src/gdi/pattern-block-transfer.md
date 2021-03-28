---
description: Il nome della funzione PatBlt (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o pattern) finché non riempie un rettangolo specificato.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Modello di trasferimento del blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993933"
---
# <a name="pattern-block-transfer"></a>Modello di trasferimento del blocco

Il nome della funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (un'abbreviazione per il trasferimento di blocchi di pattern) implica che questa funzione replica semplicemente il pennello (o pattern) finché non riempie un rettangolo specificato. Tuttavia, la funzione è in realtà molto più potente. Prima di replicare il pennello, combina i dati relativi al colore per il modello con i dati relativi al colore per i pixel esistenti sulla visualizzazione video usando un'operazione raster (POR). Un por è un'operazione bit per bit applicata ai bit dei dati relativi al colore per il pennello replicato e ai bit dei dati relativi al colore per il rettangolo di destinazione sul dispositivo di visualizzazione. Sono presenti 256 ROPs; Tuttavia, la funzione **PatBlt** riconosce solo quelle che richiedono un modello e una destinazione (non quelle che richiedono un'origine). La tabella seguente identifica il ROPs più comune.



| ROP       | Descrizione                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copia il modello nella bitmap di destinazione.                                       |
| PATINVERT | Combina la bitmap di destinazione con il modello utilizzando l'operatore booleano XOR. |
| DSTINVERT | Inverte la bitmap di destinazione.                                                     |
| NERO | Converte tutti gli output in zeri binari.                                                   |
| CANDORE | Converte tutti gli output in quelli binari.                                                    |



 

Per altre informazioni, vedere [codici operativi raster](raster-operation-codes.md).

 

 



