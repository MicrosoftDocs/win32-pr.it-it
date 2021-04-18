---
description: Rende il file specificato (EF o DF) non valido. Non è possibile accedere a un file non valido da altri metodi prima di utilizzare il ripristino.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Metodo ISCardFileAccess:: Invalidate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315876"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="a7f6c-104">Metodo ISCardFileAccess:: Invalidate</span><span class="sxs-lookup"><span data-stu-id="a7f6c-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="a7f6c-105">\[Il metodo **Invalidate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a7f6c-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a7f6c-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a7f6c-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a7f6c-108">Il metodo **Invalidate** rende il file specificato (EF o DF) non valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="a7f6c-109">Non è possibile accedere a un file non valido da altri metodi prima di utilizzare il [**ripristino**](iscardfileaccess-rehabilitate.md).</span><span class="sxs-lookup"><span data-stu-id="a7f6c-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f6c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7f6c-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="a7f6c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7f6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7f6c-112">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7f6c-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f6c-113">File.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="a7f6c-114">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7f6c-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7f6c-115">Specifica se utilizzare la messaggistica protetta.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="a7f6c-116">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="a7f6c-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7f6c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7f6c-117">Return value</span></span>

<span data-ttu-id="a7f6c-118">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a7f6c-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a7f6c-119">Return code</span></span>                                                                                   | <span data-ttu-id="a7f6c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7f6c-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a7f6c-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6c-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a7f6c-122">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a7f6c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a7f6c-124">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="a7f6c-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6c-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a7f6c-126">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a7f6c-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a7f6c-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a7f6c-128">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a7f6c-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7f6c-129">Remarks</span></span>

<span data-ttu-id="a7f6c-130">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="a7f6c-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="a7f6c-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a7f6c-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a7f6c-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a7f6c-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f6c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7f6c-133">Requirements</span></span>



| <span data-ttu-id="a7f6c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f6c-134">Requirement</span></span> | <span data-ttu-id="a7f6c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a7f6c-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7f6c-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7f6c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f6c-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7f6c-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a7f6c-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7f6c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f6c-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7f6c-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a7f6c-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a7f6c-140">End of client support</span></span><br/>    | <span data-ttu-id="a7f6c-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7f6c-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a7f6c-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a7f6c-142">End of server support</span></span><br/>    | <span data-ttu-id="a7f6c-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a7f6c-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a7f6c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7f6c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f6c-145">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="a7f6c-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="a7f6c-146">**Riabilitare**</span><span class="sxs-lookup"><span data-stu-id="a7f6c-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
