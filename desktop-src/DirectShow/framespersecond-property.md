---
description: La proprietà FramesPerSecond recupera la frequenza dei fotogrammi video per il titolo del DVD corrente.
ms.assetid: c5d36308-1447-4636-9b3a-4a3f93d27789
title: Proprietà FramesPerSecond
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00ec3281d88a2901f630c9231edbf1e76a89c23
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303966"
---
# <a name="framespersecond-property"></a>Proprietà FramesPerSecond

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `FramesPerSecond` proprietà recupera la frequenza dei fotogrammi video per il titolo del DVD corrente.

``` syntax
[ iFramesPerSec = ] MSWebDVD.FramesPerSecond
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta la frequenza dei fotogrammi video; 25 o 30 fotogrammi al secondo.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. I segnali video NTSC vengono visualizzati a 30 fotogrammi al secondo. PAL viene visualizzato a 25 fotogrammi al secondo. Un disco è codificato per la riproduzione in NTSC o PAL, ma non può essere riprodotto in entrambi i casi.

 

 



