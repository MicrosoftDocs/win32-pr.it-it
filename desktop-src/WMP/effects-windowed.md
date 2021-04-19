---
title: EFFETTI. finestra
description: L'attributo windowd specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ovvero se l'intero rettangolo del controllo sarà visibile in qualsiasi momento o se può essere ritagliato.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFETTI. finestre Media Player finestra
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333411"
---
# <a name="effectswindowed"></a><span data-ttu-id="c07bf-104">EFFETTI. finestra</span><span class="sxs-lookup"><span data-stu-id="c07bf-104">EFFECTS.windowed</span></span>

<span data-ttu-id="c07bf-105">L'attributo **windowd** specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ovvero se l'intero rettangolo del controllo sarà visibile in qualsiasi momento o se può essere ritagliato.</span><span class="sxs-lookup"><span data-stu-id="c07bf-105">The **windowed** attribute specifies or retrieves a value indicating whether the visualization will be windowed or windowless, that is, whether the entire rectangle of the control will be visible at all times, or whether it can be clipped.</span></span> <span data-ttu-id="c07bf-106">Questo attributo può essere impostato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="c07bf-106">This attribute can only be set at design time.</span></span>

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a><span data-ttu-id="c07bf-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c07bf-107">Possible Values</span></span>

<span data-ttu-id="c07bf-108">Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura in seguito.</span><span class="sxs-lookup"><span data-stu-id="c07bf-108">This attribute is a **Boolean** specified at design time and read-only thereafter.</span></span>



| <span data-ttu-id="c07bf-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c07bf-109">Value</span></span> | <span data-ttu-id="c07bf-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c07bf-110">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="c07bf-111">true</span><span class="sxs-lookup"><span data-stu-id="c07bf-111">true</span></span>  | <span data-ttu-id="c07bf-112">Il controllo sarà finestra.</span><span class="sxs-lookup"><span data-stu-id="c07bf-112">The control will be windowed.</span></span>            |
| <span data-ttu-id="c07bf-113">false</span><span class="sxs-lookup"><span data-stu-id="c07bf-113">false</span></span> | <span data-ttu-id="c07bf-114">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c07bf-114">Default.</span></span> <span data-ttu-id="c07bf-115">Il controllo sarà privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="c07bf-115">The control will be windowless.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c07bf-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c07bf-116">Remarks</span></span>

<span data-ttu-id="c07bf-117">Se si desidera una finestra di visualizzazione non rettangolare o se una parte della finestra è coperta da un'immagine, questo attributo deve essere impostato su false.</span><span class="sxs-lookup"><span data-stu-id="c07bf-117">If a non-rectangular visualization window is desired, or if any part of the window is covered by an image, this attribute must be set to false.</span></span> <span data-ttu-id="c07bf-118">In questo modo si sacrificano alcune prestazioni per eseguire il troncamento necessario.</span><span class="sxs-lookup"><span data-stu-id="c07bf-118">This sacrifices some performance to do the necessary clipping.</span></span>

<span data-ttu-id="c07bf-119">Se **la finestra è** impostata su true, qualsiasi immagine che copre la finestra di visualizzazione viene ignorata e la finestra di visualizzazione dispone dell'ordine z di livello più alto.</span><span class="sxs-lookup"><span data-stu-id="c07bf-119">If **windowed** is set to true, any image covering the visualization window is ignored, and the visualization window has the highest-level z-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07bf-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c07bf-120">Requirements</span></span>



| <span data-ttu-id="c07bf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07bf-121">Requirement</span></span> | <span data-ttu-id="c07bf-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c07bf-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c07bf-123">Versione</span><span class="sxs-lookup"><span data-stu-id="c07bf-123">Version</span></span><br/> | <span data-ttu-id="c07bf-124">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c07bf-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c07bf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c07bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07bf-126">**EFFECTs-elemento**</span><span class="sxs-lookup"><span data-stu-id="c07bf-126">**EFFECTS Element**</span></span>](effects-element.md)
</dt> </dl>

 

 





