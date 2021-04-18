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
# <a name="volumesavailable-property"></a><span data-ttu-id="d7fa6-103">Proprietà VolumesAvailable</span><span class="sxs-lookup"><span data-stu-id="d7fa6-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="d7fa6-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d7fa6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d7fa6-106">La `VolumesAvailable` proprietà recupera il numero di volumi in un set multivolume.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="d7fa6-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7fa6-107">Return Value</span></span>

<span data-ttu-id="d7fa6-108">Restituisce il numero di volumi nel set come valore integer.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fa6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7fa6-109">Remarks</span></span>

<span data-ttu-id="d7fa6-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-110">This property is read-only with no default value.</span></span> <span data-ttu-id="d7fa6-111">È possibile che alcuni titoli di DVD vengano rilasciati come serie o set multidisco.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="d7fa6-112">Utilizzare questo metodo per determinare il numero del volume del disco corrente.</span><span class="sxs-lookup"><span data-stu-id="d7fa6-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



