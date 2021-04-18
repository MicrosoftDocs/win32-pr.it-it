---
title: TEXT. fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo di testo.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- Media Player di Windows TEXT. fontStyle
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325117"
---
# <a name="textfontstyle"></a><span data-ttu-id="3d369-104">TEXT. fontStyle</span><span class="sxs-lookup"><span data-stu-id="3d369-104">TEXT.fontStyle</span></span>

<span data-ttu-id="3d369-105">L'attributo **FontStyle** specifica o recupera lo stile del carattere per il controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="3d369-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="3d369-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3d369-106">Possible Values</span></span>

<span data-ttu-id="3d369-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d369-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="3d369-108">Valore</span><span class="sxs-lookup"><span data-stu-id="3d369-108">Value</span></span>     | <span data-ttu-id="3d369-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d369-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="3d369-110">Grassetto</span><span class="sxs-lookup"><span data-stu-id="3d369-110">Bold</span></span>      | <span data-ttu-id="3d369-111">Stile del carattere in grassetto.</span><span class="sxs-lookup"><span data-stu-id="3d369-111">Bold font style.</span></span>            |
| <span data-ttu-id="3d369-112">Corsivo</span><span class="sxs-lookup"><span data-stu-id="3d369-112">Italic</span></span>    | <span data-ttu-id="3d369-113">Stile del carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="3d369-113">Italic font style.</span></span>          |
| <span data-ttu-id="3d369-114">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="3d369-114">Underline</span></span> | <span data-ttu-id="3d369-115">Stile del carattere sottolineato.</span><span class="sxs-lookup"><span data-stu-id="3d369-115">Underline font style.</span></span>       |
| <span data-ttu-id="3d369-116">Barrato</span><span class="sxs-lookup"><span data-stu-id="3d369-116">Strikeout</span></span> | <span data-ttu-id="3d369-117">Stile del carattere di attacco.</span><span class="sxs-lookup"><span data-stu-id="3d369-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="3d369-118">Normale</span><span class="sxs-lookup"><span data-stu-id="3d369-118">Normal</span></span>    | <span data-ttu-id="3d369-119">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d369-119">Default.</span></span> <span data-ttu-id="3d369-120">Stile del carattere normale.</span><span class="sxs-lookup"><span data-stu-id="3d369-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3d369-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d369-121">Remarks</span></span>

<span data-ttu-id="3d369-122">È possibile utilizzare qualsiasi combinazione di valori, separati da spazi.</span><span class="sxs-lookup"><span data-stu-id="3d369-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="3d369-123">Lo stile normale ha la priorità su tutti gli altri valori, mentre quelli specificati insieme al normale verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="3d369-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="3d369-124">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="3d369-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d369-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d369-125">Requirements</span></span>



| <span data-ttu-id="3d369-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d369-126">Requirement</span></span> | <span data-ttu-id="3d369-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3d369-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3d369-128">Versione</span><span class="sxs-lookup"><span data-stu-id="3d369-128">Version</span></span><br/> | <span data-ttu-id="3d369-129">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="3d369-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d369-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d369-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d369-131">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="3d369-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





