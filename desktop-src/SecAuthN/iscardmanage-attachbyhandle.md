---
description: Crea un collegamento di comunicazione a una smart card (ICC) utilizzando un handle restituito dal gestore di risorse della smart card.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'Metodo ISCardManage:: AttachByHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882657"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="27bba-103">Metodo ISCardManage:: AttachByHandle</span><span class="sxs-lookup"><span data-stu-id="27bba-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="27bba-104">\[Il metodo **AttachByHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="27bba-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="27bba-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="27bba-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="27bba-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="27bba-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="27bba-107">Il metodo **AttachByHandle** crea un collegamento di comunicazione a una [*Smart Card*](../secgloss/s-gly.md) (ICC) utilizzando un handle restituito dal gestore di [*risorse*](../secgloss/r-gly.md)della smart card.</span><span class="sxs-lookup"><span data-stu-id="27bba-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="27bba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27bba-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="27bba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27bba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27bba-110">*hICC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27bba-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27bba-111">Handle per una smart card.</span><span class="sxs-lookup"><span data-stu-id="27bba-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27bba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27bba-112">Return value</span></span>

<span data-ttu-id="27bba-113">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="27bba-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="27bba-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="27bba-114">Return code</span></span>                                                                                   | <span data-ttu-id="27bba-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27bba-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="27bba-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27bba-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="27bba-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="27bba-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="27bba-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="27bba-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="27bba-119">Il parametro *hICC* non è valido.</span><span class="sxs-lookup"><span data-stu-id="27bba-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="27bba-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="27bba-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="27bba-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="27bba-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="27bba-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="27bba-122">Remarks</span></span>

<span data-ttu-id="27bba-123">Per alleghi una chiamata di [*Reader*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="27bba-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="27bba-124">Per rilasciare una chiamata di allegato [**Disconnetti**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="27bba-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="27bba-125">Per riconnettersi con la smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByHandle**, chiamare [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="27bba-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="27bba-126">Per un elenco di tutti i metodi definiti dall'interfaccia [**ISCardManage**](iscardmanage.md) , vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="27bba-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="27bba-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="27bba-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="27bba-128">Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="27bba-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27bba-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27bba-129">Requirements</span></span>



| <span data-ttu-id="27bba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="27bba-130">Requirement</span></span> | <span data-ttu-id="27bba-131">Valore</span><span class="sxs-lookup"><span data-stu-id="27bba-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27bba-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27bba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="27bba-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="27bba-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="27bba-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27bba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="27bba-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27bba-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="27bba-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="27bba-136">End of client support</span></span><br/>    | <span data-ttu-id="27bba-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="27bba-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="27bba-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="27bba-138">End of server support</span></span><br/>    | <span data-ttu-id="27bba-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27bba-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="27bba-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27bba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27bba-141">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="27bba-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="27bba-142">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="27bba-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="27bba-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="27bba-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="27bba-144">**Riconnetti**</span><span class="sxs-lookup"><span data-stu-id="27bba-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
