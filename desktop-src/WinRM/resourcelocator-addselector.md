---
title: Metodo ResourceLocator. AddSelector (WSManDisp. h)
description: Aggiunge un selettore all'oggetto ResourceLocator. Il selettore specifica una particolare istanza di una risorsa.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo AddSelector
- Metodo AddSelector Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964268"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="6c3d1-107">ResourceLocator. AddSelector, metodo</span><span class="sxs-lookup"><span data-stu-id="6c3d1-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="6c3d1-108">Aggiunge un [*selettore*](windows-remote-management-glossary.md) all'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6c3d1-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="6c3d1-109">Il selettore specifica una particolare istanza di una *risorsa*.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="6c3d1-110">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="6c3d1-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3d1-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c3d1-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="6c3d1-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c3d1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3d1-113">*resourceSelName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c3d1-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3d1-114">Nome del selettore.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-114">The selector name.</span></span> <span data-ttu-id="6c3d1-115">Ad esempio, quando si richiedono dati WMI, questo parametro è la proprietà chiave per una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="6c3d1-116">*selValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c3d1-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3d1-117">Valore del selettore.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-117">The selector value.</span></span> <span data-ttu-id="6c3d1-118">Per i dati WMI, ad esempio, questo parametro contiene un valore per una proprietà chiave che identifica un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c3d1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c3d1-119">Remarks</span></span>

<span data-ttu-id="6c3d1-120">**IWSManResourceLocator:: AddSelector** è il metodo C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6c3d1-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3d1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c3d1-121">Requirements</span></span>



| <span data-ttu-id="6c3d1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3d1-122">Requirement</span></span> | <span data-ttu-id="6c3d1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6c3d1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3d1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c3d1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3d1-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c3d1-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6c3d1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c3d1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3d1-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c3d1-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6c3d1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c3d1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3d1-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d1-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c3d1-130">IDL</span><span class="sxs-lookup"><span data-stu-id="6c3d1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c3d1-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d1-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6c3d1-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c3d1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c3d1-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d1-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c3d1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6c3d1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c3d1-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c3d1-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c3d1-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c3d1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3d1-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6c3d1-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





