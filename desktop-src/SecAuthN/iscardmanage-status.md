---
description: Ottiene lo stato corrente della smart card o del lettore.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'Metodo ISCardManage:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310468"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="86dd4-103">Metodo ISCardManage:: status</span><span class="sxs-lookup"><span data-stu-id="86dd4-103">ISCardManage::Status method</span></span>

<span data-ttu-id="86dd4-104">\[Il metodo **status** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="86dd4-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86dd4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86dd4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86dd4-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="86dd4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="86dd4-107">Il metodo **status** ottiene lo stato corrente della [*Smart Card*](../secgloss/s-gly.md) o del [*lettore*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="86dd4-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86dd4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86dd4-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="86dd4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86dd4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86dd4-110">*pStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86dd4-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86dd4-111">Puntatore a un valore di \_ enumerazione degli stati spaventati.</span><span class="sxs-lookup"><span data-stu-id="86dd4-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="86dd4-112">Nell'output restituito è contenuto lo stato o lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="86dd4-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="86dd4-113">*pProtocols* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86dd4-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86dd4-114">Puntatore a un valore di \_ enumerazione di protocolli spaventati.</span><span class="sxs-lookup"><span data-stu-id="86dd4-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="86dd4-115">Nell'output restituito è contenuto il protocollo corrente.</span><span class="sxs-lookup"><span data-stu-id="86dd4-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86dd4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86dd4-116">Return value</span></span>

<span data-ttu-id="86dd4-117">Il metodo restituisce uno dei valori possibili seguenti:</span><span class="sxs-lookup"><span data-stu-id="86dd4-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="86dd4-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="86dd4-118">Return code</span></span>                                                                                   | <span data-ttu-id="86dd4-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86dd4-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="86dd4-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86dd4-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86dd4-121">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="86dd4-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="86dd4-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="86dd4-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="86dd4-123">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="86dd4-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="86dd4-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="86dd4-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="86dd4-125">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="86dd4-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="86dd4-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="86dd4-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86dd4-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="86dd4-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="86dd4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="86dd4-128">Remarks</span></span>

<span data-ttu-id="86dd4-129">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="86dd4-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="86dd4-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="86dd4-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="86dd4-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="86dd4-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86dd4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86dd4-132">Requirements</span></span>



| <span data-ttu-id="86dd4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="86dd4-133">Requirement</span></span> | <span data-ttu-id="86dd4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="86dd4-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86dd4-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86dd4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="86dd4-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="86dd4-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="86dd4-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86dd4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="86dd4-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="86dd4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="86dd4-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="86dd4-139">End of client support</span></span><br/>    | <span data-ttu-id="86dd4-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="86dd4-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="86dd4-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="86dd4-141">End of server support</span></span><br/>    | <span data-ttu-id="86dd4-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86dd4-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="86dd4-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86dd4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86dd4-144">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="86dd4-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
