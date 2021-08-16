---
description: La proprietà SubpictureStreamsAvailable recupera il numero di flussi di immagini secondarie disponibili nel titolo corrente.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Proprietà SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2349cb696c1f6d363fefb6a6e90a662fa7c3233b3b0aefcb57d381a604f41832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633441"
---
# <a name="subpicturestreamsavailable-property"></a>Proprietà SubpictureStreamsAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `SubpictureStreamsAvailable` proprietà recupera il numero di flussi di immagini secondarie disponibili nel titolo corrente.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce il numero di flussi disponibili come integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Per eseguire una query su ogni flusso per il relativo attributo di linguaggio, chiamare prima questo metodo per ottenere il limite superiore.

La numerazione dei flussi è in base zero.

 

 



