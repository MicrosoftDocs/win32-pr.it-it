---
description: Consente a un'applicazione di riconnettersi a una smart card o a un lettore senza dover eseguire una chiamata di scollegamento seguita rispettivamente da una chiamata a AttachByHandle o AttachByIFD.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Metodo ISCardManage:: Reconnect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880690"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="8e3ce-103">Metodo ISCardManage:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="8e3ce-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="8e3ce-104">\[Il metodo di **riconnessione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8e3ce-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e3ce-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8e3ce-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8e3ce-107">Il metodo **Reconnect** consente a un'applicazione di riconnettersi a una [*Smart Card*](../secgloss/s-gly.md) o a un [*lettore*](../secgloss/r-gly.md) senza dover eseguire una chiamata di [**scollegamento**](iscardmanage-detach.md) seguita rispettivamente da una chiamata a [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3ce-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3ce-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e3ce-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="8e3ce-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e3ce-109">Parameters</span></span>

<span data-ttu-id="8e3ce-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e3ce-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e3ce-111">Return value</span></span>

<span data-ttu-id="8e3ce-112">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e3ce-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="8e3ce-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8e3ce-113">Return code</span></span>                                                                                   | <span data-ttu-id="8e3ce-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e3ce-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8e3ce-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3ce-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8e3ce-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8e3ce-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8e3ce-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8e3ce-118">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8e3ce-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e3ce-119">Remarks</span></span>

<span data-ttu-id="8e3ce-120">Per connettere una smart card, chiamare [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ce-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="8e3ce-121">Per scollegare una smart card, chiamare [**Disconnetti**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ce-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="8e3ce-122">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ce-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="8e3ce-123">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8e3ce-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8e3ce-124">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ce-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3ce-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e3ce-125">Requirements</span></span>



| <span data-ttu-id="8e3ce-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e3ce-126">Requirement</span></span> | <span data-ttu-id="8e3ce-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8e3ce-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e3ce-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e3ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3ce-129">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8e3ce-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8e3ce-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e3ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3ce-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e3ce-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8e3ce-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8e3ce-132">End of client support</span></span><br/>    | <span data-ttu-id="8e3ce-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e3ce-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8e3ce-134">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8e3ce-134">End of server support</span></span><br/>    | <span data-ttu-id="8e3ce-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e3ce-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8e3ce-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e3ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3ce-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="8e3ce-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="8e3ce-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="8e3ce-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="8e3ce-139">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="8e3ce-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="8e3ce-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="8e3ce-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
