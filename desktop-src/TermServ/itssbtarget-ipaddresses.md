---
title: Proprietà ITsSbTarget IpAddresses
description: Recupera o specifica gli indirizzi IP esterni della destinazione.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetExternalIpAddresses
- Servizi Desktop remoto proprietà TargetExternalIpAddresses, interfaccia ITsSbTarget
- Servizi Desktop remoto proprietà TargetExternalIpAddresses, interfaccia ITsSbTarget
- Proprietà IpAddresses Servizi Desktop remoto
- Proprietà IpAddresses Servizi Desktop remoto, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà IpAddresses
- Proprietà IpAddresses Servizi Desktop remoto, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà IpAddresses
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397614"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="5f2cc-111">Proprietà ITsSbTarget:: IpAddresses</span><span class="sxs-lookup"><span data-stu-id="5f2cc-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="5f2cc-112">Recupera o specifica gli indirizzi IP esterni della destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="5f2cc-113">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2cc-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f2cc-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="5f2cc-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5f2cc-115">Property value</span></span>

<span data-ttu-id="5f2cc-116">Puntatore a una matrice di strutture [**tssd \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) che ricevono gli indirizzi IP esterni della destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="5f2cc-117">Puntatore a una variabile **DWORD** che contiene il numero di indirizzi IP esterni nel parametro *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="5f2cc-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="5f2cc-118">Se il numero di indirizzi è sconosciuto, passare *sockaddr* come **null**.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="5f2cc-119">Il metodo restituirà il numero di strutture [**tssd \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessarie per allocare nella matrice a cui punta il parametro *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="5f2cc-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2cc-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f2cc-120">Remarks</span></span>

<span data-ttu-id="5f2cc-121">Questa proprietà era precedentemente nota come **TargetExternalIpAddresses** in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="5f2cc-122">Se il numero di indirizzi IP esterni è sconosciuto, è possibile chiamare questo metodo con *sockaddr* impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="5f2cc-123">Il metodo restituirà quindi, nel parametro *numAddresses* , il numero di strutture [**tssd \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessarie per ricevere tutti gli indirizzi IP esterni.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="5f2cc-124">Allocare la matrice per *sockaddr* in base a questo numero, quindi chiamare di nuovo il metodo, impostando *sockaddr* sulla matrice appena allocata e *numAddresses* sul numero restituito dalla prima chiamata.</span><span class="sxs-lookup"><span data-stu-id="5f2cc-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2cc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f2cc-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f2cc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f2cc-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="5f2cc-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f2cc-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f2cc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f2cc-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="5f2cc-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f2cc-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f2cc-130">IDL</span><span class="sxs-lookup"><span data-stu-id="5f2cc-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="5f2cc-131"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="5f2cc-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f2cc-132">IID</span><span class="sxs-lookup"><span data-stu-id="5f2cc-132">IID</span></span><br/></td>
<td><span data-ttu-id="5f2cc-133">IID_ITsSbTarget viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="5f2cc-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="5f2cc-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="5f2cc-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="5f2cc-135">e85e10ea-db0b-4752-B456-5fd5840901c0 in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f2cc-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="5f2cc-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f2cc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2cc-137">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="5f2cc-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="5f2cc-138">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="5f2cc-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="5f2cc-139">**TSSD \_ ConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="5f2cc-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





