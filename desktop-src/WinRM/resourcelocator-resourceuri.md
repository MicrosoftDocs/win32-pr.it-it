---
title: Proprietà ResourceLocator. ResourceURI (WSManDisp. h)
description: Ottiene o imposta l'URI della risorsa in un oggetto ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà ResourceURI
- Gestione remota Windows proprietà ResourceURI, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477687"
---
# <a name="resourcelocatorresourceuri-property"></a><span data-ttu-id="01c29-106">Proprietà ResourceLocator. ResourceURI</span><span class="sxs-lookup"><span data-stu-id="01c29-106">ResourceLocator.ResourceURI property</span></span>

<span data-ttu-id="01c29-107">Ottiene o imposta l' [*URI della risorsa*](windows-remote-management-glossary.md) in un oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="01c29-107">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="01c29-108">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="01c29-108">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="01c29-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="01c29-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c29-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01c29-110">Syntax</span></span>


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a><span data-ttu-id="01c29-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01c29-111">Property value</span></span>

<span data-ttu-id="01c29-112">Stringa che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="01c29-112">A string that identifies the resource.</span></span> <span data-ttu-id="01c29-113">Quando si imposta l'URI della risorsa per un oggetto [**resourceLocator**](resourcelocator.md) , l'URI deve contenere solo il percorso.</span><span class="sxs-lookup"><span data-stu-id="01c29-113">When setting the resource URI for a [**ResourceLocator**](resourcelocator.md) object, the URI must contain only the path.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c29-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="01c29-114">Remarks</span></span>

<span data-ttu-id="01c29-115">Di seguito è riportato un esempio di un percorso corretto per [**resourceUri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span><span class="sxs-lookup"><span data-stu-id="01c29-115">The following is an example of a proper path for [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

<span data-ttu-id="01c29-116">Il percorso seguente non funziona perché contiene una chiave per un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="01c29-116">The following path does not work because it contains a key for a specific instance.</span></span> <span data-ttu-id="01c29-117">Usare il metodo [**resourceLocator. AddSelector**](resourcelocator-addselector.md) per specificare una particolare istanza.</span><span class="sxs-lookup"><span data-stu-id="01c29-117">Use the [**ResourceLocator.AddSelector**](resourcelocator-addselector.md) method to specify a particular instance.</span></span>

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

<span data-ttu-id="01c29-118">**IWSManResourceLocator:: ResourceURI** è il metodo C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="01c29-118">**IWSManResourceLocator::ResourceURI** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c29-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c29-119">Requirements</span></span>



| <span data-ttu-id="01c29-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c29-120">Requirement</span></span> | <span data-ttu-id="01c29-121">Valore</span><span class="sxs-lookup"><span data-stu-id="01c29-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c29-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c29-122">Minimum supported client</span></span><br/> | <span data-ttu-id="01c29-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01c29-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="01c29-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c29-124">Minimum supported server</span></span><br/> | <span data-ttu-id="01c29-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01c29-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01c29-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c29-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c29-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01c29-128">IDL</span><span class="sxs-lookup"><span data-stu-id="01c29-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01c29-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="01c29-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="01c29-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="01c29-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01c29-132">DLL</span><span class="sxs-lookup"><span data-stu-id="01c29-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c29-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01c29-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01c29-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c29-135">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="01c29-135">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





