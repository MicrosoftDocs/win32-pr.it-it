---
description: Il metodo ChangeDir imposta la directory della smart card corrente sulla nuova directory specificata.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: 'Metodo ISCardFileAccess:: ChangeDir'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 147456bd705eea3073f2e65cb375494187ca2473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879273"
---
# <a name="iscardfileaccesschangedir-method"></a><span data-ttu-id="8cf88-103">Metodo ISCardFileAccess:: ChangeDir</span><span class="sxs-lookup"><span data-stu-id="8cf88-103">ISCardFileAccess::ChangeDir method</span></span>

<span data-ttu-id="8cf88-104">\[Il metodo **ChangeDir** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8cf88-104">\[The **ChangeDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8cf88-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8cf88-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8cf88-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8cf88-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8cf88-107">Il metodo **ChangeDir** imposta la directory della [*Smart Card*](../secgloss/s-gly.md) corrente sulla nuova directory specificata.</span><span class="sxs-lookup"><span data-stu-id="8cf88-107">The **ChangeDir** method changes the current [*smart card*](../secgloss/s-gly.md) directory to the new specified directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf88-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cf88-108">Syntax</span></span>


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a><span data-ttu-id="8cf88-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cf88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf88-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cf88-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf88-111">Tipo di riferimento usato in *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="8cf88-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="8cf88-112">**\_tipo SC \_ per \_ nome**</span><span class="sxs-lookup"><span data-stu-id="8cf88-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="8cf88-113">**\_tipo SC \_ per \_ ID**</span><span class="sxs-lookup"><span data-stu-id="8cf88-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="8cf88-114">**\_tipo SC \_ per \_ breve**</span><span class="sxs-lookup"><span data-stu-id="8cf88-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="8cf88-115">**SC \_ digitare \_ per \_ qualsiasi**</span><span class="sxs-lookup"><span data-stu-id="8cf88-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="8cf88-116">*bstrNewDir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cf88-116">*bstrNewDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf88-117">Nome file/directory (da *RefType*) da selezionare.</span><span class="sxs-lookup"><span data-stu-id="8cf88-117">File/directory name (by *refType*) to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf88-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cf88-118">Return value</span></span>

<span data-ttu-id="8cf88-119">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cf88-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8cf88-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8cf88-120">Return code</span></span>                                                                                   | <span data-ttu-id="8cf88-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf88-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8cf88-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf88-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8cf88-123">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8cf88-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8cf88-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf88-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8cf88-125">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="8cf88-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8cf88-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8cf88-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8cf88-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8cf88-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8cf88-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cf88-128">Remarks</span></span>

<span data-ttu-id="8cf88-129">Per ottenere un percorso assoluto della directory attualmente selezionata, chiamare [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span><span class="sxs-lookup"><span data-stu-id="8cf88-129">To get an absolute path to the currently selected directory, call [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).</span></span>

<span data-ttu-id="8cf88-130">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="8cf88-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="8cf88-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8cf88-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8cf88-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8cf88-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf88-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cf88-133">Requirements</span></span>



| <span data-ttu-id="8cf88-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf88-134">Requirement</span></span> | <span data-ttu-id="8cf88-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8cf88-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cf88-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf88-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf88-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8cf88-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8cf88-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cf88-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf88-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cf88-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8cf88-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8cf88-140">End of client support</span></span><br/>    | <span data-ttu-id="8cf88-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8cf88-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8cf88-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8cf88-142">End of server support</span></span><br/>    | <span data-ttu-id="8cf88-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cf88-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8cf88-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cf88-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf88-145">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="8cf88-145">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[<span data-ttu-id="8cf88-146">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="8cf88-146">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
