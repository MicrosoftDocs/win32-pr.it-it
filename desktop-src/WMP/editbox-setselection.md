---
title: CASELLA. seselection
description: Il metodo di selezione Seleziona il testo nel controllo casella di modifica dall'indice iniziale specificato all'indice finale specificato.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Media Player di Windows casella. seselectation
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325865"
---
# <a name="editboxsetselection"></a><span data-ttu-id="9f5d7-104">CASELLA. seselection</span><span class="sxs-lookup"><span data-stu-id="9f5d7-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="9f5d7-105">Il metodo di **selezione** seleziona il testo nel controllo casella di modifica dall'indice iniziale specificato all'indice finale specificato.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="9f5d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f5d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5d7-107"><span id="start"></span><span id="START"></span>*iniziare*</span><span class="sxs-lookup"><span data-stu-id="9f5d7-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="9f5d7-108">**Numero** (**Long**) che contiene l'indice dei caratteri della posizione iniziale del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="9f5d7-109"><span id="end"></span><span id="END"></span>*fine*</span><span class="sxs-lookup"><span data-stu-id="9f5d7-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="9f5d7-110">**Numero** (**Long**) che contiene l'indice dei caratteri della posizione finale del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f5d7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f5d7-111">Return Value</span></span>

<span data-ttu-id="9f5d7-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f5d7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f5d7-113">Remarks</span></span>

<span data-ttu-id="9f5d7-114">Se l'inizio è 0 e la fine è 1, tutto il testo nel controllo casella di modifica viene selezionato.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="9f5d7-115">Se l'inizio è 1, viene deselezionata la selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="9f5d7-116">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="9f5d7-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f5d7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f5d7-117">Requirements</span></span>



| <span data-ttu-id="9f5d7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f5d7-118">Requirement</span></span> | <span data-ttu-id="9f5d7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9f5d7-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="9f5d7-120">Versione</span><span class="sxs-lookup"><span data-stu-id="9f5d7-120">Version</span></span><br/> | <span data-ttu-id="9f5d7-121">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="9f5d7-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f5d7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f5d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f5d7-123">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="9f5d7-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="9f5d7-124">**CASELLA. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="9f5d7-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="9f5d7-125">**CASELLA. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="9f5d7-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="9f5d7-126">**CASELLA. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="9f5d7-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





