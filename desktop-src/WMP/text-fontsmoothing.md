---
title: TESTO. fontSmoothing
description: L'attributo fontSmoothing specifica o recupera un valore che indica se la smussatura dei caratteri è abilitata.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Media Player di Windows TEXT. fontSmoothing
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325118"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="82d6a-104">TESTO. fontSmoothing</span><span class="sxs-lookup"><span data-stu-id="82d6a-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="82d6a-105">L'attributo **fontSmoothing** specifica o recupera un valore che indica se la smussatura dei caratteri è abilitata.</span><span class="sxs-lookup"><span data-stu-id="82d6a-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="82d6a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="82d6a-106">Possible Values</span></span>

<span data-ttu-id="82d6a-107">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="82d6a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="82d6a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="82d6a-108">Value</span></span> | <span data-ttu-id="82d6a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d6a-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="82d6a-110">true</span><span class="sxs-lookup"><span data-stu-id="82d6a-110">true</span></span>  | <span data-ttu-id="82d6a-111">La smussatura dei caratteri è abilitata.</span><span class="sxs-lookup"><span data-stu-id="82d6a-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="82d6a-112">false</span><span class="sxs-lookup"><span data-stu-id="82d6a-112">false</span></span> | <span data-ttu-id="82d6a-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="82d6a-113">Default.</span></span> <span data-ttu-id="82d6a-114">La smussatura dei caratteri è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="82d6a-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="82d6a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="82d6a-115">Remarks</span></span>

<span data-ttu-id="82d6a-116">La smussatura dei caratteri usa la funzionalità di anti-aliasing del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="82d6a-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="82d6a-117">Se la smussatura dei caratteri è abilitata e il sistema operativo supporta l'anti-aliasing, Windows Media Player tenta di smussare il testo.</span><span class="sxs-lookup"><span data-stu-id="82d6a-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="82d6a-118">Non tutti i tipi di carattere supportano l'anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="82d6a-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="82d6a-119">Windows Media Player 10 usa il metodo di anti-aliasing di Windows XP ClearType.</span><span class="sxs-lookup"><span data-stu-id="82d6a-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="82d6a-120">**Avviso** di La smussatura dei caratteri su un colore trasparente può causare la fusione del colore trasparente nei caratteri.</span><span class="sxs-lookup"><span data-stu-id="82d6a-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="82d6a-121">Non è consigliabile usare **fontSmoothing** se il testo verrà visualizzato su una trasparenza.</span><span class="sxs-lookup"><span data-stu-id="82d6a-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="82d6a-122">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="82d6a-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d6a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82d6a-123">Requirements</span></span>



| <span data-ttu-id="82d6a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d6a-124">Requirement</span></span> | <span data-ttu-id="82d6a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="82d6a-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="82d6a-126">Versione</span><span class="sxs-lookup"><span data-stu-id="82d6a-126">Version</span></span><br/> | <span data-ttu-id="82d6a-127">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="82d6a-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82d6a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82d6a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d6a-129">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="82d6a-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





