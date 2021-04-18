---
title: CASELLA. getSelectionEnd
description: Il metodo getSelectionEnd recupera la posizione finale del testo selezionato nel controllo casella.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- Media Player Windows casella. getSelectionEnd
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333849"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="245bf-104">CASELLA. getSelectionEnd</span><span class="sxs-lookup"><span data-stu-id="245bf-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="245bf-105">Il metodo **getSelectionEnd** recupera la posizione finale del testo selezionato nel controllo casella.</span><span class="sxs-lookup"><span data-stu-id="245bf-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="245bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="245bf-106">Parameters</span></span>

<span data-ttu-id="245bf-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="245bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="245bf-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="245bf-108">Return Value</span></span>

<span data-ttu-id="245bf-109">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="245bf-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="245bf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="245bf-110">Remarks</span></span>

<span data-ttu-id="245bf-111">Se non è selezionato alcun testo, questo metodo restituisce la posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="245bf-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="245bf-112">Se il controllo è su più righe, questo metodo restituisce l'indice dei caratteri nel controllo, non l'indice di riga.</span><span class="sxs-lookup"><span data-stu-id="245bf-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="245bf-113">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="245bf-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="245bf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="245bf-114">Requirements</span></span>



| <span data-ttu-id="245bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="245bf-115">Requirement</span></span> | <span data-ttu-id="245bf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="245bf-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="245bf-117">Versione</span><span class="sxs-lookup"><span data-stu-id="245bf-117">Version</span></span><br/> | <span data-ttu-id="245bf-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="245bf-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="245bf-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="245bf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="245bf-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="245bf-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="245bf-121">**CASELLA. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="245bf-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="245bf-122">**CASELLA. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="245bf-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="245bf-123">**CASELLA. seselection**</span><span class="sxs-lookup"><span data-stu-id="245bf-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





