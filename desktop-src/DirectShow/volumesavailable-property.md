---
description: La proprietà VolumesAvailable recupera il numero di volumi in un set multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Proprietà VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650938"
---
# <a name="volumesavailable-property"></a>Proprietà VolumesAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `VolumesAvailable` proprietà recupera il numero di volumi in un set multivolume.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce il numero di volumi nel set come Integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. Alcuni titoli DVD potrebbero essere rilasciati come set o serie multidisco. Usare questo metodo per determinare il numero di volume per il disco corrente.

 

 



