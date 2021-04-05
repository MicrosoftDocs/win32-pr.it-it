---
description: Annulla la registrazione del provider associato.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Metodo ITipAutocompleteClient:: UnadviseProvider (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882465"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a><span data-ttu-id="ac3d6-103">Metodo ITipAutocompleteClient:: UnadviseProvider</span><span class="sxs-lookup"><span data-stu-id="ac3d6-103">ITipAutocompleteClient::UnadviseProvider method</span></span>

<span data-ttu-id="ac3d6-104">Annulla la registrazione del provider associato.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-104">Unregisters the associated provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac3d6-105">Syntax</span></span>


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a><span data-ttu-id="ac3d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac3d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3d6-107">*hWndField* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac3d6-107">*hWndField* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3d6-108">Handle di finestra del campo che fornisce la funzionalità di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-108">Window handle of the field which provide the auto complete feature.</span></span>

</dd> <dt>

<span data-ttu-id="ac3d6-109">*pIACProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac3d6-109">*pIACProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3d6-110">Puntatore di interfaccia all'interfaccia del provider di completamento automatico per cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-110">Interface pointer to the auto complete provider interface to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3d6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac3d6-111">Return value</span></span>

<span data-ttu-id="ac3d6-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ac3d6-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ac3d6-113">Return code</span></span>                                                                            | <span data-ttu-id="ac3d6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac3d6-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="ac3d6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac3d6-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="ac3d6-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="ac3d6-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="ac3d6-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="ac3d6-118">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ac3d6-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac3d6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac3d6-119">Requirements</span></span>



| <span data-ttu-id="ac3d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac3d6-120">Requirement</span></span> | <span data-ttu-id="ac3d6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ac3d6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3d6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac3d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac3d6-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ac3d6-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ac3d6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac3d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac3d6-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ac3d6-125">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="ac3d6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac3d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac3d6-127"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ac3d6-127"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ac3d6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ac3d6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac3d6-129"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac3d6-129"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="ac3d6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac3d6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3d6-131">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="ac3d6-131">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> <dt>

[<span data-ttu-id="ac3d6-132">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="ac3d6-132">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




