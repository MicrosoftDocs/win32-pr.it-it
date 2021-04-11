---
description: Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Metodo ITipAutocompleteClient:: RequestShowUI (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231911"
---
# <a name="itipautocompleteclientrequestshowui-method"></a><span data-ttu-id="11001-103">Metodo ITipAutocompleteClient:: RequestShowUI</span><span class="sxs-lookup"><span data-stu-id="11001-103">ITipAutocompleteClient::RequestShowUI method</span></span>

<span data-ttu-id="11001-104">Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="11001-104">Determines whether Input Panel is ready to have the auto complete list shown.</span></span>

## <a name="syntax"></a><span data-ttu-id="11001-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11001-105">Syntax</span></span>


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a><span data-ttu-id="11001-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="11001-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11001-107">*hWndACList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11001-107">*hWndACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11001-108">Handle di finestra dell'interfaccia utente dell'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="11001-108">Window handle of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="11001-109">*pfAllowShowing* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="11001-109">*pfAllowShowing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11001-110">**False** se il client consiglia di non visualizzare l'interfaccia utente dell'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="11001-110">**FALSE** if client recommends to not show the auto complete list user interface.</span></span> <span data-ttu-id="11001-111">**True** se il provider di completamento automatico può visualizzare l'interfaccia utente dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="11001-111">**TRUE** if the auto complete provider can show the list user interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11001-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11001-112">Return value</span></span>

<span data-ttu-id="11001-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="11001-113">This method can return one of these values.</span></span>



| <span data-ttu-id="11001-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="11001-114">Return code</span></span>                                                                            | <span data-ttu-id="11001-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11001-115">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="11001-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11001-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="11001-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="11001-117">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="11001-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="11001-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="11001-119">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="11001-119">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11001-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="11001-120">Remarks</span></span>

<span data-ttu-id="11001-121">Questo metodo viene chiamato dal provider di completamento automatico quando sta per visualizzare l'interfaccia utente di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="11001-121">This method is called by the auto complete provider when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="11001-122">Se lo stato interno del client non consente al provider di visualizzare l'interfaccia utente, *pfAllowShowing* verrà impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="11001-122">If the client's internal state doesn't allow the provider to show the user interface, *pfAllowShowing* will be set to **FALSE**.</span></span> <span data-ttu-id="11001-123">Ad esempio, quando il testo viene inviato al campo dall'interfaccia della grafia nel Pannello input penna di Tablet PC e l'utente avvia immediatamente Inking, il client consiglia di non visualizzare l'interfaccia utente di completamento automatico, in modo da evitare la distruzione dell'Inking dell'utente, impostando *pfAllowShowing* su **false**.</span><span class="sxs-lookup"><span data-stu-id="11001-123">For example, when the text gets sent to the field from the handwriting skin on the Tablet PC Input Panel and the user immediately starts inking, the client will recommend to not show the auto complete user interface, in order to avoid destructing the user's inking, by setting *pfAllowShowing* to **FALSE**.</span></span>

<span data-ttu-id="11001-124">Chiamare **RequestShowUI** per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare il [**metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="11001-124">Call **RequestShowUI** to set the popup auto complete list window handle before you call the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span> <span data-ttu-id="11001-125">In caso contrario, viene generato un errore **E \_ INVALIDARG** quando si chiama **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="11001-125">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11001-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11001-126">Requirements</span></span>



| <span data-ttu-id="11001-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11001-127">Requirement</span></span> | <span data-ttu-id="11001-128">Valore</span><span class="sxs-lookup"><span data-stu-id="11001-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11001-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11001-129">Minimum supported client</span></span><br/> | <span data-ttu-id="11001-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="11001-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="11001-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11001-131">Minimum supported server</span></span><br/> | <span data-ttu-id="11001-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="11001-132">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="11001-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11001-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="11001-134"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="11001-134"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="11001-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11001-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11001-136"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11001-136"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="11001-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11001-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11001-138">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="11001-138">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="11001-139">**ITipAutocompleteClient::P metodo referredRects**</span><span class="sxs-lookup"><span data-stu-id="11001-139">**ITipAutocompleteClient::PreferredRects Method**</span></span>](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[<span data-ttu-id="11001-140">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="11001-140">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




