---
description: La proprietà Volume imposta o recupera il volume dell'altoparlante per l'output del flusso audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Proprietà Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632881"
---
# <a name="volume-property"></a>Proprietà Volume

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `Volume` proprietà imposta o recupera il volume del parlante per l'output del flusso audio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valore restituito

Restituisce il livello del volume come attenuazione in decibel come integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con un valore predefinito pari a 0. Il volume completo è 0 e 10.000 è silenzioso. la scala è logaritmica. Moltiplicare il livello di decibel desiderato per 100 (ad esempio 10.000 = 100 dB).

 

 



