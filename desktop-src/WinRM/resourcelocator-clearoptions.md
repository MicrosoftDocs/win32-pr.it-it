---
title: Metodo ResourceLocator. ClearOptions (WSManDisp. h)
description: Rimuove tutte le opzioni dall'oggetto ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo ClearOptions
- Metodo ClearOptions Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda4be766b65756a9bcf8de02a4417fd15a3e7f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873445"
---
# <a name="resourcelocatorclearoptions-method"></a><span data-ttu-id="023dd-106">ResourceLocator. ClearOptions, metodo</span><span class="sxs-lookup"><span data-stu-id="023dd-106">ResourceLocator.ClearOptions method</span></span>

<span data-ttu-id="023dd-107">Rimuove tutte le [*Opzioni*](windows-remote-management-glossary.md) dall'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="023dd-107">Removes any [*options*](windows-remote-management-glossary.md) from the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="023dd-108">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="023dd-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="023dd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="023dd-109">Syntax</span></span>


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a><span data-ttu-id="023dd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="023dd-110">Parameters</span></span>

<span data-ttu-id="023dd-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="023dd-111">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="023dd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="023dd-112">Remarks</span></span>

<span data-ttu-id="023dd-113">**IWSManResourceLocator:: ClearOptions** è il metodo C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="023dd-113">**IWSManResourceLocator::ClearOptions** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="023dd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="023dd-114">Requirements</span></span>



| <span data-ttu-id="023dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="023dd-115">Requirement</span></span> | <span data-ttu-id="023dd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="023dd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="023dd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="023dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="023dd-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="023dd-118">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="023dd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="023dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="023dd-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="023dd-120">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="023dd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="023dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="023dd-122"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="023dd-122"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="023dd-123">IDL</span><span class="sxs-lookup"><span data-stu-id="023dd-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="023dd-124"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="023dd-124"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="023dd-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="023dd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="023dd-126"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="023dd-126"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="023dd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="023dd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="023dd-128"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="023dd-128"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="023dd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="023dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="023dd-130">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="023dd-130">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





