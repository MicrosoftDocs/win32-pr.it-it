---
description: L'interfaccia IWiaPreview memorizza le immagini non filtrate internamente e le passa attraverso i filtri di elaborazione delle immagini.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interfaccia IWiaPreview (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226149"
---
# <a name="iwiapreview-interface"></a><span data-ttu-id="db079-103">Interfaccia IWiaPreview</span><span class="sxs-lookup"><span data-stu-id="db079-103">IWiaPreview interface</span></span>

<span data-ttu-id="db079-104">L'interfaccia **IWiaPreview** memorizza le immagini non filtrate internamente e le passa attraverso i filtri di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="db079-104">The **IWiaPreview** interface caches unfiltered images internally and passes them through image processing filters.</span></span>

## <a name="members"></a><span data-ttu-id="db079-105">Membri</span><span class="sxs-lookup"><span data-stu-id="db079-105">Members</span></span>

<span data-ttu-id="db079-106">L'interfaccia **IWiaPreview** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db079-106">The **IWiaPreview** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="db079-107">**IWiaPreview** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db079-107">**IWiaPreview** also has these types of members:</span></span>

-   [<span data-ttu-id="db079-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="db079-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="db079-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="db079-109">Methods</span></span>

<span data-ttu-id="db079-110">L'interfaccia **IWiaPreview** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="db079-110">The **IWiaPreview** interface has these methods.</span></span>



| <span data-ttu-id="db079-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="db079-111">Method</span></span>                                                  | <span data-ttu-id="db079-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db079-112">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db079-113">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="db079-113">**Clear**</span></span>](-wia-iwiapreview-clear.md)                 | <span data-ttu-id="db079-114">Rilascia l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="db079-114">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="db079-115">Rilascia anche il filtro di elaborazione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="db079-115">It also releases the image processing filter.</span></span> <br/>          |
| [<span data-ttu-id="db079-116">**DetectRegions**</span><span class="sxs-lookup"><span data-stu-id="db079-116">**DetectRegions**</span></span>](-wia-iwiapreview-detectregions.md) | <span data-ttu-id="db079-117">Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro.</span><span class="sxs-lookup"><span data-stu-id="db079-117">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span> <br/> |
| [<span data-ttu-id="db079-118">**GetNewPreview**</span><span class="sxs-lookup"><span data-stu-id="db079-118">**GetNewPreview**</span></span>](-wia-iwiapreview-getnewpreview.md) | <span data-ttu-id="db079-119">Memorizza nella cache internamente l'immagine non filtrata restituita dal driver.</span><span class="sxs-lookup"><span data-stu-id="db079-119">Caches internally the unfiltered image returned from the driver.</span></span> <br/>                                                                                                                |
| [<span data-ttu-id="db079-120">**UpdatePreview**</span><span class="sxs-lookup"><span data-stu-id="db079-120">**UpdatePreview**</span></span>](-wia-iwiapreview-updatepreview.md) | <span data-ttu-id="db079-121">Ottiene l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="db079-121">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="db079-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="db079-122">Remarks</span></span>

<span data-ttu-id="db079-123">Questo filtro viene chiamato automaticamente dal metodo [**IWiaTransfer::D ownload**](-wia-iwiatransfer-download.md) .</span><span class="sxs-lookup"><span data-stu-id="db079-123">This filter is called automatically by the [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) method.</span></span>

<span data-ttu-id="db079-124">L'interfaccia **IWiaPreview** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="db079-124">The **IWiaPreview** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="db079-125">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="db079-125">IUnknown Methods</span></span>                                        | <span data-ttu-id="db079-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db079-126">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="db079-127">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="db079-127">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="db079-128">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="db079-128">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="db079-129">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="db079-129">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="db079-130">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="db079-130">Increments reference count.</span></span>               |
| [<span data-ttu-id="db079-131">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="db079-131">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="db079-132">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="db079-132">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="db079-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db079-133">Requirements</span></span>



| <span data-ttu-id="db079-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="db079-134">Requirement</span></span> | <span data-ttu-id="db079-135">Valore</span><span class="sxs-lookup"><span data-stu-id="db079-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db079-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db079-136">Minimum supported client</span></span><br/> | <span data-ttu-id="db079-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db079-137">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db079-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db079-138">Minimum supported server</span></span><br/> | <span data-ttu-id="db079-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db079-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db079-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db079-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="db079-141"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="db079-141"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="db079-142">IDL</span><span class="sxs-lookup"><span data-stu-id="db079-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db079-143"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db079-143"><dt>Wia.idl</dt></span></span> </dl> |



 

 
