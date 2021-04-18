---
description: Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: Metodo ITipAutocompleteClient::P referredRects (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315565"
---
# <a name="itipautocompleteclientpreferredrects-method"></a><span data-ttu-id="4bdc8-103">ITipAutocompleteClient::P metodo referredRects</span><span class="sxs-lookup"><span data-stu-id="4bdc8-103">ITipAutocompleteClient::PreferredRects method</span></span>

<span data-ttu-id="4bdc8-104">Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-104">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bdc8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bdc8-105">Syntax</span></span>


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a><span data-ttu-id="4bdc8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bdc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdc8-107">*prcACList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4bdc8-107">*prcACList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdc8-108">Rettangolo, in coordinate dello schermo, che indica la posizione preferita del provider e le dimensioni dell'interfaccia utente dell'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-108">A rectangle, in screen coordinates, indicating the provider's preferred location and the size of the auto complete list user interface.</span></span>

</dd> <dt>

<span data-ttu-id="4bdc8-109">*prcField* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4bdc8-109">*prcField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdc8-110">Rettangolo, in coordinate dello schermo, che indica la posizione e le dimensioni del campo attivo.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-110">A rectangle, in screen coordinates, indicating the location and the size of the focused field.</span></span>

</dd> <dt>

<span data-ttu-id="4bdc8-111">*prcModified* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4bdc8-111">*prcModified* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdc8-112">Rettangolo basato sullo stato corrente della Mancia e il percorso e la dimensione dell'elenco di completamento automatico preferiti specificati da *prcACList*.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-112">A rectangle based on the current state of the TIP and the preferred auto complete list location and size specified by *prcACList*.</span></span>

</dd> <dt>

<span data-ttu-id="4bdc8-113">*pfShownAboveTip* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4bdc8-113">*pfShownAboveTip* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bdc8-114">**True** se il rettangolo modificato deve essere visualizzato sopra l'area di destinazione del pannello di input di testo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-114">**TRUE** if the modified rectangle is to be shown above the Text Input Panel's target area; otherwise, **FALSE**.</span></span> <span data-ttu-id="4bdc8-115">Questo valore deve essere inizializzato in modo da consentire l'orientamento preferito del provider prima che venga chiamato il metodo.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-115">This value must be initialized to the provider's preferred orientation before the method is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdc8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bdc8-116">Return value</span></span>

<span data-ttu-id="4bdc8-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-117">This method can return one of these values.</span></span>



| <span data-ttu-id="4bdc8-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4bdc8-118">Return code</span></span>                                                                                  | <span data-ttu-id="4bdc8-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bdc8-119">Description</span></span>                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4bdc8-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc8-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4bdc8-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-121">Success.</span></span><br/>                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="4bdc8-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc8-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4bdc8-123">Chiamare il [**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare la finestra elenco popup automatico completato prima di chiamare il [**metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md).</span><span class="sxs-lookup"><span data-stu-id="4bdc8-123">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window before calling the [**ITipAutocompleteClient::PreferredRects Method**](itipautocompleteclient-preferredrects.md).</span></span><br/> |
| <dl> <span data-ttu-id="4bdc8-124"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc8-124"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="4bdc8-125">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-125">An unspecified error occurred.</span></span><br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4bdc8-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bdc8-126">Remarks</span></span>

<span data-ttu-id="4bdc8-127">Si tratta del metodo chiamato dal provider di completamento automatico quando sta per visualizzare l'interfaccia utente di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-127">This is the method that the auto complete provider calls when it is about to show the auto complete user interface.</span></span> <span data-ttu-id="4bdc8-128">Il client modifica il rettangolo preferito del provider specificato da *prcACList* tramite l'argomento *prcModified* .</span><span class="sxs-lookup"><span data-stu-id="4bdc8-128">The client modifies the provider's preferred rectangle specified by *prcACList* through *prcModified* argument.</span></span>

<span data-ttu-id="4bdc8-129">Chiamare il [**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-129">Call the [**ITipAutocompleteClient::RequestShowUI Method**](itipautocompleteclient-requestshowui.md) to set the popup auto complete list window handle before you call **PreferredRects**.</span></span> <span data-ttu-id="4bdc8-130">In caso contrario, viene generato un errore **E \_ INVALIDARG** quando si chiama **PreferredRects**.</span><span class="sxs-lookup"><span data-stu-id="4bdc8-130">Failure to do so will cause an **E\_INVALIDARG** error when calling **PreferredRects**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bdc8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bdc8-131">Requirements</span></span>



| <span data-ttu-id="4bdc8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bdc8-132">Requirement</span></span> | <span data-ttu-id="4bdc8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4bdc8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdc8-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bdc8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4bdc8-135">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4bdc8-135">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4bdc8-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bdc8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4bdc8-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4bdc8-137">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="4bdc8-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bdc8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bdc8-139"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc8-139"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4bdc8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4bdc8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bdc8-141"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bdc8-141"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="4bdc8-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bdc8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bdc8-143">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="4bdc8-143">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="4bdc8-144">**Metodo ITipAutocompleteClient:: RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="4bdc8-144">**ITipAutocompleteClient::RequestShowUI Method**</span></span>](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[<span data-ttu-id="4bdc8-145">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="4bdc8-145">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




