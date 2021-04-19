---
description: La proprietà SubpictureStreamsAvailable Recupera il numero di flussi di immagini subimmagine disponibili nel titolo corrente.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Proprietà SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317835"
---
# <a name="subpicturestreamsavailable-property"></a>Proprietà SubpictureStreamsAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `SubpictureStreamsAvailable` proprietà recupera il numero di flussi di immagini subimmagine disponibili nel titolo corrente.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce il numero di flussi disponibili come Integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. Per eseguire una query su ogni flusso per il relativo attributo Language, chiamare innanzitutto questo metodo per ottenere il limite superiore.

La numerazione del flusso è in base zero.

 

 



