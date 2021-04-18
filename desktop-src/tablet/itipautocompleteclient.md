---
description: Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: Interfaccia ITipAutocompleteClient (TipAutoComplete. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 7b9dad38d0e3f169019934b7e60a09096aced1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318705"
---
# <a name="itipautocompleteclient-interface"></a><span data-ttu-id="69a87-103">Interfaccia ITipAutocompleteClient</span><span class="sxs-lookup"><span data-stu-id="69a87-103">ITipAutocompleteClient interface</span></span>

<span data-ttu-id="69a87-104">Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69a87-104">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span>

## <a name="members"></a><span data-ttu-id="69a87-105">Membri</span><span class="sxs-lookup"><span data-stu-id="69a87-105">Members</span></span>

<span data-ttu-id="69a87-106">L'interfaccia **ITipAutocompleteClient** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="69a87-106">The **ITipAutocompleteClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="69a87-107">**ITipAutocompleteClient** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="69a87-107">**ITipAutocompleteClient** also has these types of members:</span></span>

-   [<span data-ttu-id="69a87-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="69a87-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69a87-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="69a87-109">Methods</span></span>

<span data-ttu-id="69a87-110">L'interfaccia **ITipAutocompleteClient** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="69a87-110">The **ITipAutocompleteClient** interface has these methods.</span></span>



| <span data-ttu-id="69a87-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="69a87-111">Method</span></span>                                                              | <span data-ttu-id="69a87-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69a87-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69a87-113">**AdviseProvider**</span><span class="sxs-lookup"><span data-stu-id="69a87-113">**AdviseProvider**</span></span>](itipautocompleteclient-adviseprovider.md)     | <span data-ttu-id="69a87-114">Registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="69a87-114">Registers the provider with the client to enable the client to call the application's auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="69a87-115">**PreferredRects**</span><span class="sxs-lookup"><span data-stu-id="69a87-115">**PreferredRects**</span></span>](itipautocompleteclient-preferredrects.md)     | <span data-ttu-id="69a87-116">Consente al client di suggerire dove posizionare l'elenco di completamento automatico per evitare la sovrapposizione del pannello di input.</span><span class="sxs-lookup"><span data-stu-id="69a87-116">Allows the client to suggest where to position the auto complete list to avoid overlapping the Input Panel.</span></span><br/>                                               |
| [<span data-ttu-id="69a87-117">**RequestShowUI**</span><span class="sxs-lookup"><span data-stu-id="69a87-117">**RequestShowUI**</span></span>](itipautocompleteclient-requestshowui.md)       | <span data-ttu-id="69a87-118">Determina se il pannello di input è pronto per visualizzare l'elenco di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="69a87-118">Determines whether Input Panel is ready to have the auto complete list shown.</span></span><br/>                                                                             |
| [<span data-ttu-id="69a87-119">**UnadviseProvider**</span><span class="sxs-lookup"><span data-stu-id="69a87-119">**UnadviseProvider**</span></span>](itipautocompleteclient-unadviseprovider.md) | <span data-ttu-id="69a87-120">Annulla la registrazione del provider associato.</span><span class="sxs-lookup"><span data-stu-id="69a87-120">Unregisters the associated provider.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="69a87-121">**UserSelection**</span><span class="sxs-lookup"><span data-stu-id="69a87-121">**UserSelection**</span></span>](itipautocompleteclient-userselection.md)       | <span data-ttu-id="69a87-122">Notifica al pannello di input che l'utente ha selezionato un elemento nell'elenco di completamento automatico e per rimuovere tutto il testo rimanente che non è ancora stato inserito.</span><span class="sxs-lookup"><span data-stu-id="69a87-122">Notifies the Input Panel that the user has selected something in the auto complete list and to discard all remaining text that has not yet been inserted.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="69a87-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69a87-123">Requirements</span></span>



| <span data-ttu-id="69a87-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a87-124">Requirement</span></span> | <span data-ttu-id="69a87-125">Valore</span><span class="sxs-lookup"><span data-stu-id="69a87-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a87-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69a87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="69a87-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69a87-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="69a87-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69a87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="69a87-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69a87-129">None supported</span></span><br/>                                                                                                       |
| <span data-ttu-id="69a87-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69a87-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="69a87-131"><dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="69a87-131"><dt>TipAutoComplete.h (also requires Peninputpanel\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69a87-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69a87-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69a87-133"><dt>Tiptsf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69a87-133"><dt>Tiptsf.dll</dt></span></span> </dl>                                           |



 

