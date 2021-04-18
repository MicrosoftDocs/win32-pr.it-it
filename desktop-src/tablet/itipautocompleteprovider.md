---
description: Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: Interfaccia ITipAutocompleteProvider (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 3c300e2724ccabbc8388ef647f8f0145531cfc8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319160"
---
# <a name="itipautocompleteprovider-interface"></a><span data-ttu-id="a80ae-103">Interfaccia ITipAutocompleteProvider</span><span class="sxs-lookup"><span data-stu-id="a80ae-103">ITipAutocompleteProvider interface</span></span>

<span data-ttu-id="a80ae-104">Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.</span><span class="sxs-lookup"><span data-stu-id="a80ae-104">Manages the application's side of the Text Input Panel auto complete integration.</span></span>

## <a name="members"></a><span data-ttu-id="a80ae-105">Membri</span><span class="sxs-lookup"><span data-stu-id="a80ae-105">Members</span></span>

<span data-ttu-id="a80ae-106">L'interfaccia **ITipAutocompleteProvider** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a80ae-106">The **ITipAutocompleteProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a80ae-107">**ITipAutocompleteProvider** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a80ae-107">**ITipAutocompleteProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="a80ae-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="a80ae-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a80ae-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="a80ae-109">Methods</span></span>

<span data-ttu-id="a80ae-110">L'interfaccia **ITipAutocompleteProvider** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a80ae-110">The **ITipAutocompleteProvider** interface has these methods.</span></span>



| <span data-ttu-id="a80ae-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="a80ae-111">Method</span></span>                                                                  | <span data-ttu-id="a80ae-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a80ae-112">Description</span></span>                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a80ae-113">**Visualizza**</span><span class="sxs-lookup"><span data-stu-id="a80ae-113">**Show**</span></span>](itipautocompleteprovider-show.md)                           | <span data-ttu-id="a80ae-114">Consente di visualizzare o nascondere l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="a80ae-114">Displays or hides the auto complete list.</span></span><br/>                                                                 |
| [<span data-ttu-id="a80ae-115">**UpdatePendingText**</span><span class="sxs-lookup"><span data-stu-id="a80ae-115">**UpdatePendingText**</span></span>](itipautocompleteprovider-updatependingtext.md) | <span data-ttu-id="a80ae-116">Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.</span><span class="sxs-lookup"><span data-stu-id="a80ae-116">Used by the auto complete client to notify the application of the text a user has inked into Input Panel.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a80ae-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a80ae-117">Requirements</span></span>



| <span data-ttu-id="a80ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a80ae-118">Requirement</span></span> | <span data-ttu-id="a80ae-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a80ae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80ae-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a80ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a80ae-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a80ae-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a80ae-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a80ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a80ae-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a80ae-123">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="a80ae-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a80ae-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a80ae-125"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a80ae-125"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a80ae-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a80ae-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a80ae-127"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a80ae-127"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="a80ae-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a80ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a80ae-129">Riferimento al pannello input di testo</span><span class="sxs-lookup"><span data-stu-id="a80ae-129">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> <dt>

[<span data-ttu-id="a80ae-130">**Interfaccia ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="a80ae-130">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)
</dt> </dl>

 

