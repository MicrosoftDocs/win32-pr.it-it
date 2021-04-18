---
title: LISTBOX. popUp
description: L'attributo popUp specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- Media Player finestre LISTBOX. popUp
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327730"
---
# <a name="listboxpopup"></a><span data-ttu-id="9350c-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="9350c-104">LISTBOX.popUp</span></span>

<span data-ttu-id="9350c-105">L'attributo **popup** specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9350c-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="9350c-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9350c-106">Possible Values</span></span>

<span data-ttu-id="9350c-107">Questo attributo è un **valore booleano** specificato solo in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="9350c-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="9350c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="9350c-108">Value</span></span> | <span data-ttu-id="9350c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9350c-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="9350c-110">true</span><span class="sxs-lookup"><span data-stu-id="9350c-110">true</span></span>  | <span data-ttu-id="9350c-111">L'elemento rappresenta un controllo popup.</span><span class="sxs-lookup"><span data-stu-id="9350c-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="9350c-112">false</span><span class="sxs-lookup"><span data-stu-id="9350c-112">false</span></span> | <span data-ttu-id="9350c-113">L'elemento rappresenta un controllo casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9350c-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9350c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9350c-114">Remarks</span></span>

<span data-ttu-id="9350c-115">L'elemento **popup** rappresenta un controllo casella di riepilogo visualizzato solo quando necessario.</span><span class="sxs-lookup"><span data-stu-id="9350c-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="9350c-116">È identico all'elemento **ListBox** , ad eccezione del valore predefinito di questo attributo, che modifica il comportamento di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9350c-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="9350c-117">Per gli elementi **ListBox** , il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="9350c-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="9350c-118">Per gli elementi **popup** , il valore predefinito è true.</span><span class="sxs-lookup"><span data-stu-id="9350c-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="9350c-119">Anziché specificare questo attributo, l'elemento **ListBox** o **popup** deve essere usato in base al comportamento desiderato.</span><span class="sxs-lookup"><span data-stu-id="9350c-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="9350c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9350c-120">Requirements</span></span>



| <span data-ttu-id="9350c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9350c-121">Requirement</span></span> | <span data-ttu-id="9350c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9350c-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="9350c-123">Versione</span><span class="sxs-lookup"><span data-stu-id="9350c-123">Version</span></span><br/> | <span data-ttu-id="9350c-124">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9350c-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9350c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9350c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9350c-126">**LISTBOX (elemento)**</span><span class="sxs-lookup"><span data-stu-id="9350c-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="9350c-127">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="9350c-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





