---
title: Proprietà ResourceLocator. FragmentPath (WSManDisp. h)
description: Ottiene o imposta il percorso di una proprietà o di un frammento di risorsa quando ResourceLocator viene utilizzato nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà FragmentPath
- Gestione remota Windows proprietà FragmentPath, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048403"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="105ec-106">Proprietà ResourceLocator. FragmentPath</span><span class="sxs-lookup"><span data-stu-id="105ec-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="105ec-107">Ottiene o imposta il percorso di una proprietà o di un [*frammento*](windows-remote-management-glossary.md) di [*risorsa*](windows-remote-management-glossary.md) quando [**resourceLocator**](resourcelocator.md) viene utilizzato nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="105ec-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="105ec-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="105ec-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="105ec-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="105ec-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="105ec-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="105ec-110">Property value</span></span>

<span data-ttu-id="105ec-111">Stringa che identifica il frammento o la proprietà della risorsa.</span><span class="sxs-lookup"><span data-stu-id="105ec-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="105ec-112">Ad esempio, se la risorsa è un'unità disco e la proprietà richiesta è Manufacturer, la stringa può contenere `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="105ec-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="105ec-113">Il testo del frammento fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="105ec-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="105ec-114">In questo caso, non è possibile utilizzare `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="105ec-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="105ec-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="105ec-115">Remarks</span></span>

<span data-ttu-id="105ec-116">**IWSManResourceLocator:: FragmentPath** è la proprietà C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="105ec-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="105ec-117">È possibile specificare un elemento di una proprietà di matrice fornendo l'indice della matrice, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="105ec-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="105ec-118">Tenere presente che l'indicizzazione della matrice inizia con 1 anziché con 0.</span><span class="sxs-lookup"><span data-stu-id="105ec-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="105ec-119">Per ottenere l'intera matrice, specificare il nome della proprietà della matrice, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="105ec-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="105ec-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="105ec-120">Requirements</span></span>



| <span data-ttu-id="105ec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="105ec-121">Requirement</span></span> | <span data-ttu-id="105ec-122">Valore</span><span class="sxs-lookup"><span data-stu-id="105ec-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="105ec-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="105ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="105ec-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="105ec-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="105ec-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="105ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="105ec-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="105ec-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="105ec-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="105ec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="105ec-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="105ec-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="105ec-129">IDL</span><span class="sxs-lookup"><span data-stu-id="105ec-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="105ec-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="105ec-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="105ec-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="105ec-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="105ec-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="105ec-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="105ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="105ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105ec-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="105ec-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="105ec-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="105ec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105ec-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="105ec-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





