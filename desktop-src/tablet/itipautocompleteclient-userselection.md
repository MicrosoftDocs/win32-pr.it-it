---
description: Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'Metodo ITipAutocompleteClient:: UserSelection (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1894db9da3b8e3a36e59eb45150b27facfe0291f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313451"
---
# <a name="itipautocompleteclientuserselection-method"></a><span data-ttu-id="abba6-103">Metodo ITipAutocompleteClient:: UserSelection</span><span class="sxs-lookup"><span data-stu-id="abba6-103">ITipAutocompleteClient::UserSelection method</span></span>

<span data-ttu-id="abba6-104">Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.</span><span class="sxs-lookup"><span data-stu-id="abba6-104">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span>

## <a name="syntax"></a><span data-ttu-id="abba6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abba6-105">Syntax</span></span>


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a><span data-ttu-id="abba6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abba6-106">Parameters</span></span>

<span data-ttu-id="abba6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="abba6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abba6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abba6-108">Return value</span></span>

<span data-ttu-id="abba6-109">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="abba6-109">This method can return one of these values.</span></span>



| <span data-ttu-id="abba6-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="abba6-110">Return code</span></span>                                                                            | <span data-ttu-id="abba6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abba6-111">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="abba6-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abba6-112"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="abba6-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="abba6-113">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="abba6-114"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="abba6-114"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="abba6-115">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="abba6-115">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abba6-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="abba6-116">Remarks</span></span>

<span data-ttu-id="abba6-117">Questo metodo viene chiamato dal provider per notificare al client che è stata effettuata una selezione da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="abba6-117">This method is called from the provider to notify the client that a selection has been made by the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="abba6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abba6-118">Requirements</span></span>



| <span data-ttu-id="abba6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="abba6-119">Requirement</span></span> | <span data-ttu-id="abba6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="abba6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abba6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abba6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="abba6-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="abba6-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="abba6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abba6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="abba6-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="abba6-124">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="abba6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abba6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="abba6-126"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="abba6-126"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="abba6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="abba6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abba6-128"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abba6-128"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="abba6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abba6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abba6-130">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="abba6-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="abba6-131">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="abba6-131">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




