---
description: La proprietà CurrentVolume Recupera il numero di volume per la directory radice corrente.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Proprietà CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303770"
---
# <a name="currentvolume-property"></a>Proprietà CurrentVolume

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentVolume` proprietà recupera il numero di volume per la directory radice corrente.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il volume DVD corrente. Se un disco fa parte di un set di più volumi, il valore intero deve essere maggiore di zero.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



