---
description: Crea un collegamento di comunicazione a un Reader, usando un nome visualizzato fornito per il lettore.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'Metodo ISCardManage:: AttachByIFD'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313731"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="ce952-103">Metodo ISCardManage:: AttachByIFD</span><span class="sxs-lookup"><span data-stu-id="ce952-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="ce952-104">\[Il metodo **AttachByIFD** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ce952-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ce952-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ce952-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ce952-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ce952-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ce952-107">Il metodo **AttachByIFD** crea un collegamento di comunicazione a un [*Reader*](../secgloss/r-gly.md), usando un nome visualizzato fornito per il lettore.</span><span class="sxs-lookup"><span data-stu-id="ce952-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce952-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce952-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="ce952-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce952-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce952-110">*bstrIFDName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce952-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce952-111">Nome visualizzato del lettore.</span><span class="sxs-lookup"><span data-stu-id="ce952-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce952-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce952-112">Return value</span></span>

<span data-ttu-id="ce952-113">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce952-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="ce952-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ce952-114">Return code</span></span>                                                                                   | <span data-ttu-id="ce952-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce952-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ce952-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce952-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ce952-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ce952-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="ce952-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ce952-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ce952-119">Il parametro *bstrIFDName* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ce952-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ce952-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ce952-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ce952-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ce952-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ce952-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce952-122">Remarks</span></span>

<span data-ttu-id="ce952-123">Per alleghi una [*Smart Card*](../secgloss/s-gly.md) , chiamare [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span><span class="sxs-lookup"><span data-stu-id="ce952-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="ce952-124">Per rilasciare una chiamata di allegato [**Disconnetti**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="ce952-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="ce952-125">Per riconnettersi con la smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByIFD**, chiamare [**Reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="ce952-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="ce952-126">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="ce952-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="ce952-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ce952-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ce952-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ce952-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce952-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce952-129">Requirements</span></span>



| <span data-ttu-id="ce952-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce952-130">Requirement</span></span> | <span data-ttu-id="ce952-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ce952-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce952-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce952-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce952-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ce952-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ce952-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce952-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce952-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce952-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce952-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ce952-136">End of client support</span></span><br/>    | <span data-ttu-id="ce952-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce952-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="ce952-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ce952-138">End of server support</span></span><br/>    | <span data-ttu-id="ce952-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce952-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="ce952-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce952-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce952-141">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="ce952-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="ce952-142">**Scollegare**</span><span class="sxs-lookup"><span data-stu-id="ce952-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="ce952-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="ce952-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="ce952-144">**Riconnetti**</span><span class="sxs-lookup"><span data-stu-id="ce952-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
