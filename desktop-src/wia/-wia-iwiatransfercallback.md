---
description: L'interfaccia IWiaTransferCallback riceve i callback durante il trasferimento dei dati.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interfaccia IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129410"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="af0c1-103">Interfaccia IWiaTransferCallback</span><span class="sxs-lookup"><span data-stu-id="af0c1-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="af0c1-104">L'interfaccia **IWiaTransferCallback** riceve i callback durante il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="af0c1-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="af0c1-105">Membri</span><span class="sxs-lookup"><span data-stu-id="af0c1-105">Members</span></span>

<span data-ttu-id="af0c1-106">L'interfaccia **IWiaTransferCallback** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="af0c1-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="af0c1-107">**IWiaTransferCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af0c1-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="af0c1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="af0c1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af0c1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="af0c1-109">Methods</span></span>

<span data-ttu-id="af0c1-110">L'interfaccia **IWiaTransferCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af0c1-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="af0c1-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="af0c1-111">Method</span></span>                                                                 | <span data-ttu-id="af0c1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af0c1-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="af0c1-113">**GetNextStream**</span><span class="sxs-lookup"><span data-stu-id="af0c1-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="af0c1-114">Ottiene un nuovo flusso per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="af0c1-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="af0c1-115">**TransferCallback**</span><span class="sxs-lookup"><span data-stu-id="af0c1-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="af0c1-116">Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.</span><span class="sxs-lookup"><span data-stu-id="af0c1-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="af0c1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="af0c1-117">Remarks</span></span>

<span data-ttu-id="af0c1-118">Gli sviluppatori del filtro per l'elaborazione delle immagini devono implementare questa interfaccia e l'interfaccia [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="af0c1-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="af0c1-119">L'interfaccia **IWiaTransferCallback** , come tutte le interfacce Component Object Model (com), eredita i metodi di interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="af0c1-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="af0c1-120">Metodi IUnknown</span><span class="sxs-lookup"><span data-stu-id="af0c1-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="af0c1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af0c1-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="af0c1-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="af0c1-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="af0c1-123">Restituisce puntatori alle interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="af0c1-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="af0c1-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="af0c1-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="af0c1-125">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="af0c1-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="af0c1-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="af0c1-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="af0c1-127">Riduce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="af0c1-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="af0c1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af0c1-128">Requirements</span></span>



| <span data-ttu-id="af0c1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="af0c1-129">Requirement</span></span> | <span data-ttu-id="af0c1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="af0c1-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af0c1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af0c1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="af0c1-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af0c1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="af0c1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af0c1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="af0c1-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af0c1-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af0c1-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af0c1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="af0c1-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="af0c1-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="af0c1-137">IDL</span><span class="sxs-lookup"><span data-stu-id="af0c1-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af0c1-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af0c1-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="af0c1-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="af0c1-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="af0c1-140"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af0c1-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
