---
description: La proprietà VolumesAvailable Recupera il numero di volumi in un set multivolume.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Proprietà VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314366"
---
# <a name="volumesavailable-property"></a>Proprietà VolumesAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `VolumesAvailable` proprietà recupera il numero di volumi in un set multivolume.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce il numero di volumi nel set come valore integer.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. È possibile che alcuni titoli di DVD vengano rilasciati come serie o set multidisco. Utilizzare questo metodo per determinare il numero del volume del disco corrente.

 

 



