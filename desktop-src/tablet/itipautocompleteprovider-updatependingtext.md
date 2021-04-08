---
description: Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Metodo ITipAutocompleteProvider:: UpdatePendingText (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058332"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a><span data-ttu-id="b4eea-103">Metodo ITipAutocompleteProvider:: UpdatePendingText</span><span class="sxs-lookup"><span data-stu-id="b4eea-103">ITipAutocompleteProvider::UpdatePendingText method</span></span>

<span data-ttu-id="b4eea-104">Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.</span><span class="sxs-lookup"><span data-stu-id="b4eea-104">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4eea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4eea-105">Syntax</span></span>


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a><span data-ttu-id="b4eea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4eea-107">*bstrPendingText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4eea-107">*bstrPendingText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4eea-108">Testo di origine da usare per generare l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="b4eea-108">Source text to be used to generate the auto complete list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4eea-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4eea-109">Return value</span></span>

<span data-ttu-id="b4eea-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b4eea-110">This method can return one of these values.</span></span>



| <span data-ttu-id="b4eea-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b4eea-111">Return code</span></span>                                                                            | <span data-ttu-id="b4eea-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4eea-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="b4eea-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4eea-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="b4eea-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b4eea-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="b4eea-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="b4eea-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="b4eea-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b4eea-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4eea-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4eea-117">Remarks</span></span>

<span data-ttu-id="b4eea-118">Questo testo non conterrà il testo già inserito nel campo con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b4eea-118">This text will not contain the text already inserted in the focused field.</span></span> <span data-ttu-id="b4eea-119">Il provider di completamento automatico è responsabile di prendere in considerazione il testo del campo corrente e la selezione per generare l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="b4eea-119">The auto complete provider is responsible for taking into account the current field text and the selection to generate the auto complete list.</span></span> <span data-ttu-id="b4eea-120">Quando *bstrPendingText* è **null**, l'elenco di completamento automatico viene generato con il testo corrente a sinistra della selezione nel campo.</span><span class="sxs-lookup"><span data-stu-id="b4eea-120">When *bstrPendingText* is **NULL**, the auto complete list is generated with the current text to the left of the selection in the field.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4eea-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4eea-121">Requirements</span></span>



| <span data-ttu-id="b4eea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4eea-122">Requirement</span></span> | <span data-ttu-id="b4eea-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b4eea-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4eea-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b4eea-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b4eea-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="b4eea-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4eea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b4eea-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b4eea-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="b4eea-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4eea-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4eea-129"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4eea-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4eea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b4eea-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4eea-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4eea-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="b4eea-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4eea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4eea-133">**Interfaccia ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="b4eea-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="b4eea-134">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="b4eea-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




