---
description: Consente di visualizzare o nascondere l'elenco di completamento automatico.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Metodo ITipAutocompleteProvider:: Show (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759815"
---
# <a name="itipautocompleteprovidershow-method"></a><span data-ttu-id="31633-103">Metodo ITipAutocompleteProvider:: Show</span><span class="sxs-lookup"><span data-stu-id="31633-103">ITipAutocompleteProvider::Show method</span></span>

<span data-ttu-id="31633-104">Consente di visualizzare o nascondere l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="31633-104">Displays or hides the auto complete list.</span></span>

## <a name="syntax"></a><span data-ttu-id="31633-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31633-105">Syntax</span></span>


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a><span data-ttu-id="31633-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="31633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31633-107">*fShow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31633-107">*fShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31633-108">**True** per visualizzare l'interfaccia utente di completamento automatico, **false** per nascondere l'interfaccia utente dell'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="31633-108">**TRUE** to show the auto complete user interface, **FALSE** to hide the auto complete list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31633-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31633-109">Return value</span></span>

<span data-ttu-id="31633-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="31633-110">This method can return one of these values.</span></span>



| <span data-ttu-id="31633-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="31633-111">Return code</span></span>                                                                            | <span data-ttu-id="31633-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31633-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="31633-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31633-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="31633-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="31633-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="31633-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="31633-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="31633-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="31633-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31633-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="31633-117">Remarks</span></span>

<span data-ttu-id="31633-118">Questo metodo viene chiamato dal client per mostrare o nascondere l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="31633-118">This method is called by the client to show or hide the auto complete list.</span></span> <span data-ttu-id="31633-119">Se l'elenco di completamento automatico non viene visualizzato e *fShow* è **false**, questo metodo non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="31633-119">If the auto complete list is not displayed and *fShow* is **FALSE**, this method does nothing.</span></span> <span data-ttu-id="31633-120">Se viene visualizzato l'elenco di completamento automatico e *fShow* è **true**, questo metodo non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="31633-120">If the auto complete list is displayed and *fShow* is **TRUE**, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="31633-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31633-121">Requirements</span></span>



| <span data-ttu-id="31633-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="31633-122">Requirement</span></span> | <span data-ttu-id="31633-123">Valore</span><span class="sxs-lookup"><span data-stu-id="31633-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31633-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31633-124">Minimum supported client</span></span><br/> | <span data-ttu-id="31633-125">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="31633-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="31633-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31633-126">Minimum supported server</span></span><br/> | <span data-ttu-id="31633-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="31633-127">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="31633-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31633-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="31633-129"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="31633-129"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31633-130">DLL</span><span class="sxs-lookup"><span data-stu-id="31633-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31633-131"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31633-131"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="31633-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31633-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31633-133">**Interfaccia ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="31633-133">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)
</dt> <dt>

[<span data-ttu-id="31633-134">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="31633-134">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




