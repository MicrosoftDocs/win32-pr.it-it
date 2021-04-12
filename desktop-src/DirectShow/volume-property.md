---
description: La proprietà volume imposta o Recupera il volume del altoparlante per l'output del flusso audio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Proprietà Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527805"
---
# <a name="volume-property"></a>Proprietà Volume

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `Volume` proprietà imposta o Recupera il volume del altoparlante per l'output del flusso audio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valore restituito

Restituisce il livello del volume come attenuazione in decibel come valore integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è 0. Il volume completo è 0 e 10.000 è silenzioso; la scala è logaritmica. Moltiplicare il livello di decibel desiderato di 100 (ad esempio, 10.000 = 100 dB).

 

 



