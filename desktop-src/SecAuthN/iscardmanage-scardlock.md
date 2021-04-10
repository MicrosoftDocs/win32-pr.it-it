---
description: Blocca una smart card connessa per l'uso esclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Metodo ISCardManage:: SCardLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226961"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="bb6ab-103">Metodo ISCardManage:: SCardLock</span><span class="sxs-lookup"><span data-stu-id="bb6ab-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="bb6ab-104">\[Il metodo **SCardLock** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb6ab-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb6ab-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bb6ab-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bb6ab-107">Il metodo **SCardLock** blocca una [*Smart Card*](../secgloss/s-gly.md) connessa per un uso esclusivo.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb6ab-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="bb6ab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb6ab-109">Parameters</span></span>

<span data-ttu-id="bb6ab-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb6ab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb6ab-111">Return value</span></span>

<span data-ttu-id="bb6ab-112">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb6ab-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="bb6ab-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bb6ab-113">Return code</span></span>                                                                            | <span data-ttu-id="bb6ab-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb6ab-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bb6ab-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ab-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bb6ab-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bb6ab-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ab-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bb6ab-118">Non è stato possibile completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="bb6ab-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb6ab-119">Remarks</span></span>

<span data-ttu-id="bb6ab-120">Per rilasciare l'utilizzo esclusivo della smart card connessa, chiamare [**SCardUnlock**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="bb6ab-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="bb6ab-121">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="bb6ab-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="bb6ab-122">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bb6ab-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bb6ab-123">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bb6ab-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6ab-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb6ab-124">Requirements</span></span>



| <span data-ttu-id="bb6ab-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb6ab-125">Requirement</span></span> | <span data-ttu-id="bb6ab-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bb6ab-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb6ab-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb6ab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6ab-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb6ab-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="bb6ab-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb6ab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6ab-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb6ab-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bb6ab-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb6ab-131">End of client support</span></span><br/>    | <span data-ttu-id="bb6ab-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb6ab-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="bb6ab-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bb6ab-133">End of server support</span></span><br/>    | <span data-ttu-id="bb6ab-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb6ab-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bb6ab-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb6ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6ab-136">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="bb6ab-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="bb6ab-137">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="bb6ab-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
