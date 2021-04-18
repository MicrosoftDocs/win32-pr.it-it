---
title: CASELLA. fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo casella di modifica.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- Media Player Windows casella. fontStyle
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324745"
---
# <a name="editboxfontstyle"></a><span data-ttu-id="ff0f9-104">CASELLA. fontStyle</span><span class="sxs-lookup"><span data-stu-id="ff0f9-104">EDITBOX.fontStyle</span></span>

<span data-ttu-id="ff0f9-105">L'attributo **FontStyle** specifica o recupera lo stile del carattere per il controllo casella di modifica.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-105">The **fontStyle** attribute specifies or retrieves the font style for the edit box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="ff0f9-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ff0f9-106">Possible Values</span></span>

<span data-ttu-id="ff0f9-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="ff0f9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="ff0f9-108">Value</span></span>     | <span data-ttu-id="ff0f9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff0f9-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="ff0f9-110">Grassetto</span><span class="sxs-lookup"><span data-stu-id="ff0f9-110">Bold</span></span>      | <span data-ttu-id="ff0f9-111">Stile del carattere in grassetto.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-111">Bold font style.</span></span>      |
| <span data-ttu-id="ff0f9-112">Corsivo</span><span class="sxs-lookup"><span data-stu-id="ff0f9-112">Italic</span></span>    | <span data-ttu-id="ff0f9-113">Stile del carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-113">Italic font style.</span></span>    |
| <span data-ttu-id="ff0f9-114">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="ff0f9-114">Underline</span></span> | <span data-ttu-id="ff0f9-115">Stile del carattere sottolineato.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-115">Underline font style.</span></span> |
| <span data-ttu-id="ff0f9-116">Barrato</span><span class="sxs-lookup"><span data-stu-id="ff0f9-116">Strikeout</span></span> | <span data-ttu-id="ff0f9-117">Stile del carattere di attacco.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-117">Strikeout font style.</span></span> |
| <span data-ttu-id="ff0f9-118">Normale</span><span class="sxs-lookup"><span data-stu-id="ff0f9-118">Normal</span></span>    | <span data-ttu-id="ff0f9-119">Stile del carattere normale.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="ff0f9-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff0f9-120">Remarks</span></span>

<span data-ttu-id="ff0f9-121">È possibile utilizzare qualsiasi combinazione di valori, separati da spazi.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="ff0f9-122">Lo stile normale ha la priorità su tutti gli altri valori, mentre quelli specificati insieme al normale verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="ff0f9-123">A scopo di rendering, Normal è lo stile del tipo di carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff0f9-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="ff0f9-124">Il valore predefinito recuperato da questo attributo è "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="ff0f9-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0f9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff0f9-125">Requirements</span></span>



| <span data-ttu-id="ff0f9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0f9-126">Requirement</span></span> | <span data-ttu-id="ff0f9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ff0f9-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="ff0f9-128">Versione</span><span class="sxs-lookup"><span data-stu-id="ff0f9-128">Version</span></span><br/> | <span data-ttu-id="ff0f9-129">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ff0f9-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff0f9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff0f9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0f9-131">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="ff0f9-131">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="ff0f9-132">**CASELLA. fontFace**</span><span class="sxs-lookup"><span data-stu-id="ff0f9-132">**EDITBOX.fontFace**</span></span>](editbox-fontface.md)
</dt> <dt>

[<span data-ttu-id="ff0f9-133">**CASELLA. fontSize**</span><span class="sxs-lookup"><span data-stu-id="ff0f9-133">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> </dl>

 

 





