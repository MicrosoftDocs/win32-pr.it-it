---
title: Identificatori del tipo di spazio colore
description: Queste costanti specificano il tipo di una matrice di spazi dei colori PostScript 2. I valori seguenti sono tipi di matrice di spazi dei colori validi.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320181"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="bb449-104">Identificatori del tipo di spazio colore</span><span class="sxs-lookup"><span data-stu-id="bb449-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="bb449-105">Queste costanti specificano il tipo di una matrice di spazi dei colori PostScript 2.</span><span class="sxs-lookup"><span data-stu-id="bb449-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="bb449-106">I valori seguenti sono tipi di matrice di spazi dei colori validi.</span><span class="sxs-lookup"><span data-stu-id="bb449-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="bb449-107"><span id="CSA_A"></span><span id="csa_a"></span>**\_A CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-108">Ottiene una matrice di spazi dei colori CIEBasedA dal profilo monocromatico.</span><span class="sxs-lookup"><span data-stu-id="bb449-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_grigio CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-110">Ottiene una matrice di spazi dei colori CIEBasedA dal profilo monocromatico.</span><span class="sxs-lookup"><span data-stu-id="bb449-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**\_ABC CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-112">Ottenere una matrice di spazi dei colori CIEBasedABC dal profilo RGB o L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bb449-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**DEF. CSA \_**</span><span class="sxs-lookup"><span data-stu-id="bb449-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-114">Ottenere una matrice di spazi dei colori CIEBasedDEF dal profilo RGB o L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bb449-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**\_RGB CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-116">Ottiene una matrice di spazi dei colori CIEBasedDEF seguita da una matrice di spazi dei colori CIEBasedABC dal profilo RGB.</span><span class="sxs-lookup"><span data-stu-id="bb449-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="bb449-117">In caso di esecuzione, se la stampante non supporta spazi dei colori CIEBasedDEF, la funzione utilizza la definizione CIEBasedABC.</span><span class="sxs-lookup"><span data-stu-id="bb449-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratorio CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-119">Ottiene una matrice di spazi dei colori CIEBasedABC dal <sup>\*</sup> profilo L a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="bb449-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_defg CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-121">Ottiene una matrice di spazi dei colori CIEBasedDEFG dal profilo CMYK.</span><span class="sxs-lookup"><span data-stu-id="bb449-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb449-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**\_CMYK CSA**</span><span class="sxs-lookup"><span data-stu-id="bb449-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb449-123">Ottiene una matrice di spazi dei colori CIEBasedCMYK dal profilo CMYK.</span><span class="sxs-lookup"><span data-stu-id="bb449-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bb449-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb449-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb449-125">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="bb449-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="bb449-126">Costanti ICM</span><span class="sxs-lookup"><span data-stu-id="bb449-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




