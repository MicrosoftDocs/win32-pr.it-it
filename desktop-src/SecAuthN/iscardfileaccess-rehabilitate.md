---
description: Rende un file (EF o DF) precedentemente reso non valido utilizzando il metodo Invalidate, accessibile dall'applicazione.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'Metodo ISCardFileAccess:: recovere'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312828"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="05059-103">Metodo ISCardFileAccess:: recovere</span><span class="sxs-lookup"><span data-stu-id="05059-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="05059-104">\[Il metodo di **ripristino** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="05059-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="05059-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="05059-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="05059-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="05059-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="05059-107">Il **Metodo** Recoverable rende un file (EF o DF) precedentemente reso non valido tramite il metodo [**Invalidate**](iscardfileaccess-invalidate.md) , accessibile dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="05059-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="05059-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05059-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="05059-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="05059-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05059-110">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05059-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05059-111">File da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="05059-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="05059-112">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05059-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05059-113">Specifica se utilizzare la messaggistica protetta.</span><span class="sxs-lookup"><span data-stu-id="05059-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="05059-114">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="05059-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05059-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05059-115">Return value</span></span>

<span data-ttu-id="05059-116">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="05059-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="05059-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="05059-117">Return code</span></span>                                                                                   | <span data-ttu-id="05059-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05059-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="05059-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05059-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="05059-120">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="05059-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="05059-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05059-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="05059-122">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="05059-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="05059-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="05059-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05059-124">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="05059-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="05059-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="05059-125">Remarks</span></span>

<span data-ttu-id="05059-126">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="05059-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="05059-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="05059-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="05059-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="05059-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05059-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05059-129">Requirements</span></span>



| <span data-ttu-id="05059-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="05059-130">Requirement</span></span> | <span data-ttu-id="05059-131">Valore</span><span class="sxs-lookup"><span data-stu-id="05059-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05059-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05059-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05059-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="05059-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="05059-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05059-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05059-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="05059-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="05059-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="05059-136">End of client support</span></span><br/>    | <span data-ttu-id="05059-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="05059-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="05059-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="05059-138">End of server support</span></span><br/>    | <span data-ttu-id="05059-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05059-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="05059-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05059-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05059-141">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="05059-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="05059-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="05059-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
