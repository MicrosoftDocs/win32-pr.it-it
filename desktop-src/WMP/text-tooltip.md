---
title: TESTO. toolTip
description: L'attributo toolTip specifica o Recupera il testo della descrizione comando per il controllo di testo.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TESTO. toolTip Media Player Windows
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327605"
---
# <a name="texttooltip"></a><span data-ttu-id="c84c1-104">TESTO. toolTip</span><span class="sxs-lookup"><span data-stu-id="c84c1-104">TEXT.toolTip</span></span>

<span data-ttu-id="c84c1-105">L'attributo **ToolTip** specifica o Recupera il testo della descrizione comando per il controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="c84c1-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="c84c1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c84c1-106">Possible Values</span></span>

<span data-ttu-id="c84c1-107">Questo attributo è una **stringa** di lettura/scrittura con una lunghezza massima di 1024 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c84c1-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="c84c1-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c84c1-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84c1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c84c1-109">Remarks</span></span>

<span data-ttu-id="c84c1-110">Se questo attributo non viene specificato e il testo nell'attributo **value** viene troncato nel controllo testo, o **WordWrap** è impostato su true, la descrizione comando visualizzerà il testo completo dell'attributo **value** .</span><span class="sxs-lookup"><span data-stu-id="c84c1-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="c84c1-111">Quando questo attributo è impostato su "" (stringa vuota), non viene visualizzata alcuna descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="c84c1-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="c84c1-112">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="c84c1-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84c1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c84c1-113">Requirements</span></span>



| <span data-ttu-id="c84c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84c1-114">Requirement</span></span> | <span data-ttu-id="c84c1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c84c1-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c84c1-116">Versione</span><span class="sxs-lookup"><span data-stu-id="c84c1-116">Version</span></span><br/> | <span data-ttu-id="c84c1-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c84c1-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c84c1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c84c1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84c1-119">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="c84c1-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="c84c1-120">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="c84c1-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="c84c1-121">**TESTO. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="c84c1-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





