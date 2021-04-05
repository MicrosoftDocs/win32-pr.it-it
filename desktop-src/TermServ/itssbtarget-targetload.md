---
title: Proprietà TargetLoad di ITsSbTarget
description: Recupera il carico relativo in una destinazione.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetLoad
- Servizi Desktop remoto proprietà TargetLoad, interfaccia ITsSbTarget
- Interfaccia ITsSbTarget Servizi Desktop remoto, proprietà TargetLoad
- Servizi Desktop remoto proprietà TargetLoad, interfaccia ITsSbTargetEx
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, proprietà TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718583"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="a489c-108">Proprietà ITsSbTarget:: TargetLoad</span><span class="sxs-lookup"><span data-stu-id="a489c-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="a489c-109">Recupera il carico relativo in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="a489c-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="a489c-110">Questo valore è basato sul numero di sessioni esistenti e in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a489c-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="a489c-111">Per impostazione predefinita, una sessione in sospeso ha lo stesso valore di una sessione esistente.</span><span class="sxs-lookup"><span data-stu-id="a489c-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="a489c-112">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a489c-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a489c-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a489c-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="a489c-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a489c-114">Property value</span></span>

<span data-ttu-id="a489c-115">Numero che rappresenta il carico relativo in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="a489c-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="a489c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a489c-116">Remarks</span></span>

<span data-ttu-id="a489c-117">Il peso di una sessione in sospeso relativa a una sessione attiva può essere modificato impostando il valore del parametro *lb \_ ConnectionEstablishmentPenalty* per il gestore connessione.</span><span class="sxs-lookup"><span data-stu-id="a489c-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="a489c-118">Questo parametro si trova nella chiave del registro di **\\ sistema HKLM System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="a489c-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="a489c-119">Il valore predefinito 1 indica che le sessioni in sospeso hanno lo stesso peso delle sessioni attive.</span><span class="sxs-lookup"><span data-stu-id="a489c-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="a489c-120">Questa proprietà è disponibile in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato nell'interfaccia [**ITsSbTargetEx**](itssbtargetex.md) .</span><span class="sxs-lookup"><span data-stu-id="a489c-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a489c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a489c-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a489c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a489c-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="a489c-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a489c-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a489c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a489c-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="a489c-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a489c-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a489c-126">IDL</span><span class="sxs-lookup"><span data-stu-id="a489c-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="a489c-127"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="a489c-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a489c-128">IID</span><span class="sxs-lookup"><span data-stu-id="a489c-128">IID</span></span><br/></td>
<td><span data-ttu-id="a489c-129">IID_ITsSbTarget viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="a489c-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="a489c-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="a489c-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="a489c-131">e85e10ea-db0b-4752-B456-5fd5840901c0 in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a489c-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="a489c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a489c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a489c-133">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="a489c-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="a489c-134">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="a489c-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





