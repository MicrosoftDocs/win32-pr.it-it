---
description: L' \_ enumerazione MXDC S0 \_ Page \_ Enumerations viene utilizzata per specificare i tipi di risorse che possono essere associati alle pagine nei documenti XPS e che possono essere elaborati, o passati non elaborati, da Microsoft XPS Document Converter (MXDC) all'output.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumerazione MXDC_S0_PAGE_ENUMS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881602"
---
# <a name="mxdc_s0_page_enums-enumeration"></a><span data-ttu-id="b4b4e-103">Enumerazione enumerazioni della \_ pagina S0 MXDC \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4b4e-103">MXDC\_S0\_PAGE\_ENUMS enumeration</span></span>

<span data-ttu-id="b4b4e-104">L'enumerazione **MXDC \_ S0 \_ Page \_ Enumerations** viene utilizzata per specificare i tipi di risorse che possono essere associati alle pagine nei documenti XPS e che possono essere elaborati, o passati non elaborati, da Microsoft XPS Document Converter (MXDC) all'output.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-104">The **MXDC\_S0\_PAGE\_ENUMS** enumeration is used to specify types of resources that can be associated with pages in XPS documents and that can be processed, or passed unprocessed, by Microsoft XPS Document Converter (MXDC) to its output.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b4e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4b4e-105">Syntax</span></span>


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a><span data-ttu-id="b4b4e-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b4b4e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b4b4e-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**\_ttf risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-107"><span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**MXDC\_RESOURCE\_TTF**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-108">Tipo di carattere TrueType o OpenType.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-108">TrueType or OpenType font.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC di \_ risorse \_ JPEG**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-109"><span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC\_RESOURCE\_JPEG**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-110">Immagine JPEG</span><span class="sxs-lookup"><span data-stu-id="b4b4e-110">JPEG image</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**\_png risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-111"><span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC\_RESOURCE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-112">Immagine PNG.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-112">PNG image.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**\_TIFF risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-113"><span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC\_RESOURCE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-114">Immagine TIFF.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-114">TIFF image.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**\_WDP risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-115"><span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC\_RESOURCE\_WDP**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-116">Immagine foto di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-116">Windows Media Photo image.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_dizionario risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-117"><span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**MXDC\_RESOURCE\_DICTIONARY**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-118">Dizionario risorse remoto da passare all'output di MXDC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-118">Remote resource dictionary that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ profilo ICC della risorsa MXDC \_**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-119"><span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**MXDC\_RESOURCE\_ICC\_PROFILE**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-120">Profilo ICC da passare all'output di MXDC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-120">ICC profile that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**\_ \_ Anteprima JPEG risorsa \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-121"><span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC\_RESOURCE\_JPEG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-122">Anteprima JPEG da passare all'output di MXDC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-122">JPEG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**\_ \_ Anteprima png risorse \_ MXDC**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-123"><span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC\_RESOURCE\_PNG\_THUMBNAIL**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-124">Anteprima PNG da passare all'output di MXDC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-124">PNG thumbnail that should be passed to MXDC's output unprocessed.</span></span>

</dd> <dt>

<span data-ttu-id="b4b4e-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ risorsa \_ massima**</span><span class="sxs-lookup"><span data-stu-id="b4b4e-125"><span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC\_RESOURCE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="b4b4e-126">Numero massimo di risorse per la convalida.</span><span class="sxs-lookup"><span data-stu-id="b4b4e-126">The maximum resource count for validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4b4e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4b4e-127">Remarks</span></span>

<span data-ttu-id="b4b4e-128">Questa enumerazione viene utilizzata principalmente come membro **dwResourceType** della struttura della [**\_ \_ \_ risorsa \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="b4b4e-128">This enumeration is primarily used as the **dwResourceType** member of the [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b4e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4b4e-129">Requirements</span></span>



| <span data-ttu-id="b4b4e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b4e-130">Requirement</span></span> | <span data-ttu-id="b4b4e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b4b4e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b4e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4b4e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b4e-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4b4e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b4b4e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4b4e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b4e-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4b4e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b4b4e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4b4e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b4e-137"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4b4e-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




