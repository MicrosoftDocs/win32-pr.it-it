---
title: Metodo ResourceLocator. ClearSelectors (WSManDisp. h)
description: Rimuove tutti i selettori da un oggetto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo ClearSelectors
- Metodo ClearSelectors Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121070"
---
# <a name="resourcelocatorclearselectors-method"></a><span data-ttu-id="6988b-106">ResourceLocator. ClearSelectors, metodo</span><span class="sxs-lookup"><span data-stu-id="6988b-106">ResourceLocator.ClearSelectors method</span></span>

<span data-ttu-id="6988b-107">Rimuove tutti i [*selettori*](windows-remote-management-glossary.md) da un oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6988b-107">Removes all of the [*selectors*](windows-remote-management-glossary.md) from a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="6988b-108">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="6988b-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6988b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6988b-109">Syntax</span></span>


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a><span data-ttu-id="6988b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6988b-110">Parameters</span></span>

<span data-ttu-id="6988b-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6988b-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6988b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6988b-112">Remarks</span></span>

<span data-ttu-id="6988b-113">**IWSManResourceLocator:: ClearSelectors** è il metodo C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6988b-113">**IWSManResourceLocator::ClearSelectors** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6988b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6988b-114">Requirements</span></span>



| <span data-ttu-id="6988b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6988b-115">Requirement</span></span> | <span data-ttu-id="6988b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6988b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6988b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6988b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6988b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6988b-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6988b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6988b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6988b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6988b-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6988b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6988b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6988b-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6988b-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6988b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="6988b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6988b-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6988b-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6988b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="6988b-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6988b-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6988b-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6988b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6988b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6988b-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6988b-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6988b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6988b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6988b-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6988b-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





