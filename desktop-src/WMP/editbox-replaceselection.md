---
title: CASELLA. replaceSelection
description: Il metodo replaceSelection sostituisce la selezione corrente con il testo specificato.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Media Player Windows casella. replaceSelection
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325866"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="49547-104">CASELLA. replaceSelection</span><span class="sxs-lookup"><span data-stu-id="49547-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="49547-105">Il metodo **replaceSelection** sostituisce la selezione corrente con il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="49547-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="49547-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49547-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span><span class="sxs-lookup"><span data-stu-id="49547-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="49547-108">**Stringa** contenente il testo in cui sostituire il testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="49547-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49547-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49547-109">Return Value</span></span>

<span data-ttu-id="49547-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="49547-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49547-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="49547-111">Remarks</span></span>

<span data-ttu-id="49547-112">Se non è selezionato alcun testo, il testo di sostituzione viene inserito nella posizione corrente del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="49547-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="49547-113">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="49547-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="49547-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49547-114">Requirements</span></span>



| <span data-ttu-id="49547-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="49547-115">Requirement</span></span> | <span data-ttu-id="49547-116">Valore</span><span class="sxs-lookup"><span data-stu-id="49547-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="49547-117">Versione</span><span class="sxs-lookup"><span data-stu-id="49547-117">Version</span></span><br/> | <span data-ttu-id="49547-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="49547-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49547-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49547-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49547-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="49547-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="49547-121">**CASELLA. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="49547-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="49547-122">**CASELLA. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="49547-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="49547-123">**CASELLA. seselection**</span><span class="sxs-lookup"><span data-stu-id="49547-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





