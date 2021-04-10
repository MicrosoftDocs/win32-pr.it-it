---
description: Il metodo Open apre il file specificato per un ulteriore utilizzo.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'Metodo ISCardFileAccess:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131455"
---
# <a name="iscardfileaccessopen-method"></a><span data-ttu-id="a84f9-103">Metodo ISCardFileAccess:: Open</span><span class="sxs-lookup"><span data-stu-id="a84f9-103">ISCardFileAccess::Open method</span></span>

<span data-ttu-id="a84f9-104">\[Il metodo **Open** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a84f9-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a84f9-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a84f9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a84f9-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a84f9-107">Il metodo **Open** apre il file specificato per un ulteriore utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a84f9-107">The **Open** method opens the specified file for further use.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84f9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a84f9-108">Syntax</span></span>


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a><span data-ttu-id="a84f9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a84f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84f9-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84f9-111">Tipo di riferimento usato in *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="a84f9-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="a84f9-112">**\_tipo SC \_ per \_ nome**</span><span class="sxs-lookup"><span data-stu-id="a84f9-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="a84f9-113">**\_tipo SC \_ per \_ ID**</span><span class="sxs-lookup"><span data-stu-id="a84f9-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="a84f9-114">**\_tipo SC \_ per \_ breve**</span><span class="sxs-lookup"><span data-stu-id="a84f9-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="a84f9-115">**SC \_ digitare \_ per \_ qualsiasi**</span><span class="sxs-lookup"><span data-stu-id="a84f9-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a84f9-116">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84f9-117">File da aprire.</span><span class="sxs-lookup"><span data-stu-id="a84f9-117">File to open.</span></span>

</dd> <dt>

<span data-ttu-id="a84f9-118">*phFile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-118">*phFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a84f9-119">Puntatore a un file HSCARD che conterrà \_ l'handle di file.</span><span class="sxs-lookup"><span data-stu-id="a84f9-119">Pointer to an HSCARD\_FILE that will hold the file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a84f9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a84f9-120">Return value</span></span>

<span data-ttu-id="a84f9-121">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a84f9-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a84f9-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a84f9-122">Return code</span></span>                                                                                   | <span data-ttu-id="a84f9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a84f9-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a84f9-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a84f9-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a84f9-125">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a84f9-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a84f9-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a84f9-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a84f9-127">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a84f9-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a84f9-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a84f9-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a84f9-129">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="a84f9-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a84f9-130"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a84f9-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a84f9-131">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a84f9-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a84f9-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="a84f9-132">Remarks</span></span>

<span data-ttu-id="a84f9-133">Per chiudere un file, chiamare [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="a84f9-133">To close a file, call [**Close**](iscardfileaccess-close.md).</span></span>

<span data-ttu-id="a84f9-134">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="a84f9-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="a84f9-135">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a84f9-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a84f9-136">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a84f9-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a84f9-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a84f9-137">Requirements</span></span>



| <span data-ttu-id="a84f9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a84f9-138">Requirement</span></span> | <span data-ttu-id="a84f9-139">Valore</span><span class="sxs-lookup"><span data-stu-id="a84f9-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a84f9-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a84f9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a84f9-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a84f9-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a84f9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a84f9-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a84f9-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a84f9-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a84f9-144">End of client support</span></span><br/>    | <span data-ttu-id="a84f9-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a84f9-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a84f9-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a84f9-146">End of server support</span></span><br/>    | <span data-ttu-id="a84f9-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a84f9-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a84f9-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a84f9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84f9-149">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="a84f9-149">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="a84f9-150">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="a84f9-150">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
