---
description: Reimposta il contesto di sicurezza corrente della smart card.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'Metodo ISCardVerify:: ResetSecurityState'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878622"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="795dd-103">Metodo ISCardVerify:: ResetSecurityState</span><span class="sxs-lookup"><span data-stu-id="795dd-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="795dd-104">\[Il metodo **ResetSecurityState** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="795dd-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="795dd-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="795dd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="795dd-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="795dd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="795dd-107">Il metodo **ResetSecurityState** Reimposta il contesto di [*sicurezza*](../secgloss/s-gly.md) corrente della [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="795dd-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="795dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="795dd-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="795dd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="795dd-109">Parameters</span></span>

<span data-ttu-id="795dd-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="795dd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="795dd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="795dd-111">Return value</span></span>

<span data-ttu-id="795dd-112">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="795dd-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="795dd-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="795dd-113">Return code</span></span>                                                                                   | <span data-ttu-id="795dd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="795dd-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="795dd-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="795dd-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="795dd-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="795dd-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="795dd-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="795dd-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="795dd-118">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="795dd-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="795dd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="795dd-119">Remarks</span></span>

<span data-ttu-id="795dd-120">Per abilitare di nuovo il [*contesto di sicurezza*](../secgloss/s-gly.md) senza reimpostare, chiamare [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="795dd-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="795dd-121">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="795dd-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="795dd-122">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="795dd-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="795dd-123">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="795dd-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="795dd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="795dd-124">Requirements</span></span>



| <span data-ttu-id="795dd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="795dd-125">Requirement</span></span> | <span data-ttu-id="795dd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="795dd-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="795dd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="795dd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="795dd-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="795dd-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="795dd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="795dd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="795dd-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="795dd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="795dd-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="795dd-131">End of client support</span></span><br/>    | <span data-ttu-id="795dd-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="795dd-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="795dd-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="795dd-133">End of server support</span></span><br/>    | <span data-ttu-id="795dd-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="795dd-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="795dd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="795dd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795dd-136">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="795dd-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="795dd-137">[**Sbloccare**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="795dd-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
