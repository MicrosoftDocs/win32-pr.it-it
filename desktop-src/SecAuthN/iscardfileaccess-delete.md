---
description: Il metodo Delete Elimina un file in una posizione specificata all'interno della smart card file system.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: ISCardFileAccess::D Metodo Elimina
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343601"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="fe01c-103">ISCardFileAccess::D Metodo Elimina</span><span class="sxs-lookup"><span data-stu-id="fe01c-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="fe01c-104">\[Il metodo **Delete** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fe01c-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fe01c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe01c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe01c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fe01c-107">Il metodo **Delete** Elimina un file in una posizione specificata all'interno della [*Smart Card*](../secgloss/s-gly.md) file System.</span><span class="sxs-lookup"><span data-stu-id="fe01c-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe01c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe01c-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="fe01c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe01c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe01c-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe01c-111">Tipo di riferimento usato in *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="fe01c-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="fe01c-112">**\_tipo SC \_ per \_ nome**</span><span class="sxs-lookup"><span data-stu-id="fe01c-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="fe01c-113">**\_tipo SC \_ per \_ ID**</span><span class="sxs-lookup"><span data-stu-id="fe01c-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="fe01c-114">**\_tipo SC \_ per \_ breve**</span><span class="sxs-lookup"><span data-stu-id="fe01c-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="fe01c-115">**SC \_ digitare \_ per \_ qualsiasi**</span><span class="sxs-lookup"><span data-stu-id="fe01c-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="fe01c-116">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe01c-117">Identificatore del file da eliminare.</span><span class="sxs-lookup"><span data-stu-id="fe01c-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="fe01c-118">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe01c-119">Specifica se è necessario utilizzare la messaggistica protetta e i dati preallocati.</span><span class="sxs-lookup"><span data-stu-id="fe01c-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fe01c-120">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="fe01c-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="fe01c-121">**SC \_ FL \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="fe01c-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe01c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe01c-122">Return value</span></span>

<span data-ttu-id="fe01c-123">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe01c-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fe01c-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe01c-124">Return code</span></span>                                                                                  | <span data-ttu-id="fe01c-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe01c-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="fe01c-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="fe01c-127">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="fe01c-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="fe01c-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="fe01c-129">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="fe01c-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="fe01c-130"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe01c-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="fe01c-131">L'interfaccia non ha implementato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fe01c-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe01c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe01c-132">Remarks</span></span>

<span data-ttu-id="fe01c-133">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fe01c-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fe01c-134">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fe01c-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fe01c-135">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fe01c-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe01c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe01c-136">Requirements</span></span>



| <span data-ttu-id="fe01c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe01c-137">Requirement</span></span> | <span data-ttu-id="fe01c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="fe01c-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe01c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe01c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fe01c-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fe01c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe01c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fe01c-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe01c-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fe01c-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fe01c-143">End of client support</span></span><br/>    | <span data-ttu-id="fe01c-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe01c-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fe01c-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fe01c-145">End of server support</span></span><br/>    | <span data-ttu-id="fe01c-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe01c-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fe01c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe01c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe01c-148">**Creare**</span><span class="sxs-lookup"><span data-stu-id="fe01c-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="fe01c-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="fe01c-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
