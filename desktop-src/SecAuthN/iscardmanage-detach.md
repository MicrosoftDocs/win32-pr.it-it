---
description: Rilascia l'allegato a una smart card o un lettore specifico allocato rispettivamente da AttachByHandle e AttachByIFD.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage::D Metodo etach
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130654"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="89aa9-103">ISCardManage::D Metodo etach</span><span class="sxs-lookup"><span data-stu-id="89aa9-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="89aa9-104">\[Il metodo **Detach** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="89aa9-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="89aa9-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89aa9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89aa9-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="89aa9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="89aa9-107">Il metodo **Detach** rilascia l'allegato a una [*Smart Card*](../secgloss/s-gly.md) o a un [*lettore*](../secgloss/r-gly.md) specifico allocato rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) e [**AttachByIFD**](iscardmanage-attachbyifd.md) .</span><span class="sxs-lookup"><span data-stu-id="89aa9-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="89aa9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89aa9-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="89aa9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89aa9-109">Parameters</span></span>

<span data-ttu-id="89aa9-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="89aa9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89aa9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89aa9-111">Return value</span></span>

<span data-ttu-id="89aa9-112">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="89aa9-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="89aa9-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="89aa9-113">Return code</span></span>                                                                                   | <span data-ttu-id="89aa9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89aa9-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="89aa9-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89aa9-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="89aa9-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="89aa9-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="89aa9-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="89aa9-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="89aa9-118">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="89aa9-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="89aa9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="89aa9-119">Remarks</span></span>

<span data-ttu-id="89aa9-120">Per connettere una smart card, chiamare [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="89aa9-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="89aa9-121">Per riconnettersi con la smart card senza chiamare **Detach** e [**AttachByHandle**](iscardmanage-attachbyhandle.md), chiamare [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="89aa9-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="89aa9-122">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="89aa9-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="89aa9-123">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="89aa9-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="89aa9-124">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="89aa9-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89aa9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89aa9-125">Requirements</span></span>



| <span data-ttu-id="89aa9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="89aa9-126">Requirement</span></span> | <span data-ttu-id="89aa9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="89aa9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89aa9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89aa9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="89aa9-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="89aa9-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="89aa9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89aa9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="89aa9-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89aa9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89aa9-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="89aa9-132">End of client support</span></span><br/>    | <span data-ttu-id="89aa9-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="89aa9-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="89aa9-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="89aa9-134">End of server support</span></span><br/>    | <span data-ttu-id="89aa9-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89aa9-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="89aa9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89aa9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89aa9-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="89aa9-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="89aa9-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="89aa9-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="89aa9-139">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="89aa9-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="89aa9-140">**Riconnetti**</span><span class="sxs-lookup"><span data-stu-id="89aa9-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
