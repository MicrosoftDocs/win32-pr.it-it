---
title: Proprietà ResourceLocator. MustUnderstandOptions (WSManDisp. h)
description: Ottiene o imposta il valore MustUnderstandOptions per l'oggetto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà MustUnderstandOptions
- Gestione remota Windows proprietà MustUnderstandOptions, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964803"
---
# <a name="resourcelocatormustunderstandoptions-property"></a><span data-ttu-id="580a1-106">Proprietà ResourceLocator. MustUnderstandOptions</span><span class="sxs-lookup"><span data-stu-id="580a1-106">ResourceLocator.MustUnderstandOptions property</span></span>

<span data-ttu-id="580a1-107">Ottiene o imposta il valore **MustUnderstandOptions** per l'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="580a1-107">Gets or sets the **MustUnderstandOptions** value for the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="580a1-108">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="580a1-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="580a1-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="580a1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="580a1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="580a1-110">Syntax</span></span>


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a><span data-ttu-id="580a1-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="580a1-111">Property value</span></span>

<span data-ttu-id="580a1-112">Indica, quando **true**, che il servizio che implementa l' [protocollo WS-Management](ws-management-protocol.md) deve restituire un errore se non è in grado di elaborare l'opzione.</span><span class="sxs-lookup"><span data-stu-id="580a1-112">Indicates, when **True**, that the service which implements the [WS-Management Protocol](ws-management-protocol.md) must return an error if it is not capable of processing the option.</span></span>

## <a name="remarks"></a><span data-ttu-id="580a1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="580a1-113">Remarks</span></span>

<span data-ttu-id="580a1-114">**IWSManResourceLocator:: MustUnderstandOptions** è la proprietà C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="580a1-114">**IWSManResourceLocator::MustUnderstandOptions** is the corresponding C++ property.</span></span>

## <a name="requirements"></a><span data-ttu-id="580a1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="580a1-115">Requirements</span></span>



| <span data-ttu-id="580a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="580a1-116">Requirement</span></span> | <span data-ttu-id="580a1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="580a1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="580a1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="580a1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="580a1-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="580a1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="580a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="580a1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="580a1-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="580a1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="580a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="580a1-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="580a1-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="580a1-124">IDL</span><span class="sxs-lookup"><span data-stu-id="580a1-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="580a1-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="580a1-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="580a1-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="580a1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="580a1-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="580a1-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="580a1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="580a1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="580a1-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="580a1-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="580a1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="580a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580a1-131">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="580a1-131">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





