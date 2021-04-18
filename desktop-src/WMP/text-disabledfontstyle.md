---
title: TESTO. disabledFontStyle
description: L'attributo disabledFontStyle specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando è disabilitato.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Media Player di Windows TEXT. disabledFontStyle
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329596"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="197f6-104">TESTO. disabledFontStyle</span><span class="sxs-lookup"><span data-stu-id="197f6-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="197f6-105">L'attributo **disabledFontStyle** specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="197f6-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="197f6-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="197f6-106">Possible Values</span></span>

<span data-ttu-id="197f6-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="197f6-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="197f6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="197f6-108">Value</span></span>     | <span data-ttu-id="197f6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="197f6-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="197f6-110">Grassetto</span><span class="sxs-lookup"><span data-stu-id="197f6-110">Bold</span></span>      | <span data-ttu-id="197f6-111">Stile del carattere in grassetto.</span><span class="sxs-lookup"><span data-stu-id="197f6-111">Bold font style.</span></span>      |
| <span data-ttu-id="197f6-112">Corsivo</span><span class="sxs-lookup"><span data-stu-id="197f6-112">Italic</span></span>    | <span data-ttu-id="197f6-113">Stile del carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="197f6-113">Italic font style.</span></span>    |
| <span data-ttu-id="197f6-114">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="197f6-114">Underline</span></span> | <span data-ttu-id="197f6-115">Stile del carattere sottolineato.</span><span class="sxs-lookup"><span data-stu-id="197f6-115">Underline font style.</span></span> |
| <span data-ttu-id="197f6-116">Barrato</span><span class="sxs-lookup"><span data-stu-id="197f6-116">Strikeout</span></span> | <span data-ttu-id="197f6-117">Stile del carattere di attacco.</span><span class="sxs-lookup"><span data-stu-id="197f6-117">Strikeout font style.</span></span> |
| <span data-ttu-id="197f6-118">Normale</span><span class="sxs-lookup"><span data-stu-id="197f6-118">Normal</span></span>    | <span data-ttu-id="197f6-119">Stile del carattere normale.</span><span class="sxs-lookup"><span data-stu-id="197f6-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="197f6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="197f6-120">Remarks</span></span>

<span data-ttu-id="197f6-121">È possibile utilizzare qualsiasi combinazione di valori, separati da spazi.</span><span class="sxs-lookup"><span data-stu-id="197f6-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="197f6-122">Lo stile normale ha la priorità su tutti gli altri valori, mentre quelli specificati insieme al normale verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="197f6-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="197f6-123">Se **disabledFontStyle** non è specificato, viene utilizzato **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="197f6-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="197f6-124">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="197f6-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="197f6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="197f6-125">Requirements</span></span>



| <span data-ttu-id="197f6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="197f6-126">Requirement</span></span> | <span data-ttu-id="197f6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="197f6-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="197f6-128">Versione</span><span class="sxs-lookup"><span data-stu-id="197f6-128">Version</span></span><br/> | <span data-ttu-id="197f6-129">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="197f6-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="197f6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="197f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197f6-131">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="197f6-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="197f6-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="197f6-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





