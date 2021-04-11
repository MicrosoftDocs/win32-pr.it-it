---
description: Rilascia l'utilizzo esclusivo della smart card connessa.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Metodo ISCardManage:: SCardUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226959"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="42d8f-103">Metodo ISCardManage:: SCardUnlock</span><span class="sxs-lookup"><span data-stu-id="42d8f-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="42d8f-104">\[Il metodo **SCardUnlock** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="42d8f-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="42d8f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42d8f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="42d8f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="42d8f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="42d8f-107">Il metodo **SCardUnlock** rilascia l'utilizzo esclusivo della [*Smart Card*](../secgloss/s-gly.md)connessa.</span><span class="sxs-lookup"><span data-stu-id="42d8f-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42d8f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42d8f-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="42d8f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="42d8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d8f-110">*Disposizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42d8f-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d8f-111">Stato in cui lasciare la smart card al rilascio del blocco.</span><span class="sxs-lookup"><span data-stu-id="42d8f-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="42d8f-112">**LASCIARE**</span><span class="sxs-lookup"><span data-stu-id="42d8f-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="42d8f-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="42d8f-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="42d8f-114">**Non alimentato**</span><span class="sxs-lookup"><span data-stu-id="42d8f-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="42d8f-115">**EJECT**</span><span class="sxs-lookup"><span data-stu-id="42d8f-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d8f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42d8f-116">Return value</span></span>

<span data-ttu-id="42d8f-117">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="42d8f-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="42d8f-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="42d8f-118">Return code</span></span>                                                                                  | <span data-ttu-id="42d8f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42d8f-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="42d8f-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42d8f-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="42d8f-121">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="42d8f-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="42d8f-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="42d8f-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="42d8f-123">Il parametro *Disposition* non è valido.</span><span class="sxs-lookup"><span data-stu-id="42d8f-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42d8f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="42d8f-124">Remarks</span></span>

<span data-ttu-id="42d8f-125">Per bloccare la smart card connessa, chiamare [**SCardLock**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="42d8f-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="42d8f-126">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="42d8f-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="42d8f-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="42d8f-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="42d8f-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="42d8f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42d8f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42d8f-129">Requirements</span></span>



| <span data-ttu-id="42d8f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d8f-130">Requirement</span></span> | <span data-ttu-id="42d8f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="42d8f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42d8f-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42d8f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="42d8f-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42d8f-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="42d8f-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42d8f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="42d8f-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42d8f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="42d8f-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="42d8f-136">End of client support</span></span><br/>    | <span data-ttu-id="42d8f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="42d8f-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="42d8f-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="42d8f-138">End of server support</span></span><br/>    | <span data-ttu-id="42d8f-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42d8f-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="42d8f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42d8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d8f-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="42d8f-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="42d8f-142">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="42d8f-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
