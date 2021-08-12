---
description: La proprietà CurrentVolume recupera il numero di volume per la directory radice corrente.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Proprietà CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654603"
---
# <a name="currentvolume-property"></a>Proprietà CurrentVolume

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentVolume` proprietà recupera il numero di volume per la directory radice corrente.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il volume DVD corrente. Se un disco fa parte di un set con più volumi, il valore intero deve essere maggiore di zero.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**VolumiDisponibili**](volumesavailable-property.md)
</dt> </dl>

 

 



