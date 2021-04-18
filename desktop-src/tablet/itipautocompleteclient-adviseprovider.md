---
description: Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Metodo ITipAutocompleteClient:: AdviseProvider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313454"
---
# <a name="itipautocompleteclientadviseprovider-method"></a><span data-ttu-id="12518-103">Metodo ITipAutocompleteClient:: AdviseProvider</span><span class="sxs-lookup"><span data-stu-id="12518-103">ITipAutocompleteClient::AdviseProvider method</span></span>

<span data-ttu-id="12518-104">Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="12518-104">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12518-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12518-105">Syntax</span></span>


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="12518-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12518-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12518-107">*hWndField* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12518-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12518-108">Handle della finestra del campo che fornisce la funzionalità di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="12518-108">The window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="12518-109">*pIACProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12518-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12518-110">Puntatore di interfaccia all'interfaccia del provider di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="12518-110">The interface pointer to the auto complete provider interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12518-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12518-111">Return value</span></span>

<span data-ttu-id="12518-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="12518-112">This method can return one of these values.</span></span>



| <span data-ttu-id="12518-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="12518-113">Return code</span></span>                                                                            | <span data-ttu-id="12518-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12518-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="12518-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="12518-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="12518-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="12518-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="12518-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="12518-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="12518-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="12518-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12518-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12518-119">Requirements</span></span>



| <span data-ttu-id="12518-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12518-120">Requirement</span></span> | <span data-ttu-id="12518-121">Valore</span><span class="sxs-lookup"><span data-stu-id="12518-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12518-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12518-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12518-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="12518-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="12518-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12518-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12518-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="12518-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="12518-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12518-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12518-127"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12518-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12518-128">DLL</span><span class="sxs-lookup"><span data-stu-id="12518-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12518-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12518-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="12518-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12518-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12518-131">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="12518-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="12518-132">**Metodo ITipAutocompleteClient:: UnadviseProvider**</span><span class="sxs-lookup"><span data-stu-id="12518-132">**ITipAutocompleteClient::UnadviseProvider Method**</span></span>](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[<span data-ttu-id="12518-133">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="12518-133">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




