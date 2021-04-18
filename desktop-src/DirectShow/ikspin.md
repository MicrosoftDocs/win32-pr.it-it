---
description: L'interfaccia IKsPin fornisce un metodo per recuperare i supporti supportati da un pin in un filtro in modalità kernel. IKsPin dispone di metodi aggiuntivi oltre a quello illustrato di seguito, ma non sono supportati per DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interfaccia IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303999"
---
# <a name="ikspin-interface"></a><span data-ttu-id="9e068-104">Interfaccia IKsPin</span><span class="sxs-lookup"><span data-stu-id="9e068-104">IKsPin interface</span></span>

<span data-ttu-id="9e068-105">L' `IKsPin` interfaccia fornisce un metodo per recuperare i supporti supportati da un pin in un filtro in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="9e068-105">The `IKsPin` interface provides a method to retrieve the mediums supported by a pin on a kernel-mode filter.</span></span> <span data-ttu-id="9e068-106">`IKsPin` dispone di metodi aggiuntivi oltre a quelli illustrati in questo argomento, ma non sono supportati per DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9e068-106">`IKsPin` has additional methods besides the one shown here, but they are not supported for DirectShow.</span></span>

## <a name="members"></a><span data-ttu-id="9e068-107">Membri</span><span class="sxs-lookup"><span data-stu-id="9e068-107">Members</span></span>

<span data-ttu-id="9e068-108">L'interfaccia **IKsPin** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9e068-108">The **IKsPin** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9e068-109">**IKsPin** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e068-109">**IKsPin** also has these types of members:</span></span>

-   [<span data-ttu-id="9e068-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e068-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9e068-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e068-111">Methods</span></span>

<span data-ttu-id="9e068-112">L'interfaccia **IKsPin** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9e068-112">The **IKsPin** interface has these methods.</span></span>



| <span data-ttu-id="9e068-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e068-113">Method</span></span>                                          | <span data-ttu-id="9e068-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e068-114">Description</span></span>                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="9e068-115">**KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="9e068-115">**KsQueryMediums**</span></span>](ikspin-ksquerymediums.md) | <span data-ttu-id="9e068-116">Recupera i supporti supportati da un PIN.</span><span class="sxs-lookup"><span data-stu-id="9e068-116">Retrieves the mediums supported by a pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e068-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e068-117">Remarks</span></span>

<span data-ttu-id="9e068-118">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="9e068-118">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e068-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e068-119">Requirements</span></span>



| <span data-ttu-id="9e068-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e068-120">Requirement</span></span> | <span data-ttu-id="9e068-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9e068-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e068-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e068-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9e068-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e068-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9e068-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e068-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9e068-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e068-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e068-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e068-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e068-127"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e068-127"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="9e068-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e068-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e068-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e068-129"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
