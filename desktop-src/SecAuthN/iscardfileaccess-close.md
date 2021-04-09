---
description: Il metodo Close chiude il file specificato. Non sono consentiti altri accessi al file.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: 'Metodo ISCardFileAccess:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: ac08d62e71045df49503eb4c05fcb5ea273b4cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129322"
---
# <a name="iscardfileaccessclose-method"></a><span data-ttu-id="9eb70-104">Metodo ISCardFileAccess:: Close</span><span class="sxs-lookup"><span data-stu-id="9eb70-104">ISCardFileAccess::Close method</span></span>

<span data-ttu-id="9eb70-105">\[Il metodo **Close** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9eb70-105">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9eb70-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9eb70-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9eb70-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9eb70-108">Il metodo **Close** chiude il file specificato.</span><span class="sxs-lookup"><span data-stu-id="9eb70-108">The **Close** method closes the specified file.</span></span> <span data-ttu-id="9eb70-109">Non sono consentiti altri accessi al file.</span><span class="sxs-lookup"><span data-stu-id="9eb70-109">No further access to file is allowed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb70-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb70-110">Syntax</span></span>


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="9eb70-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eb70-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb70-112">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-112">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb70-113">Handle per il file da chiudere.</span><span class="sxs-lookup"><span data-stu-id="9eb70-113">A handle to the file to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb70-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eb70-114">Return value</span></span>

<span data-ttu-id="9eb70-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="9eb70-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9eb70-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9eb70-116">Return code</span></span>                                                                                   | <span data-ttu-id="9eb70-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eb70-117">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9eb70-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9eb70-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9eb70-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9eb70-119">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9eb70-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9eb70-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9eb70-121">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="9eb70-121">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9eb70-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9eb70-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9eb70-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9eb70-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9eb70-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eb70-124">Remarks</span></span>

<span data-ttu-id="9eb70-125">Per aprire un file, chiamare [**Apri**](iscardfileaccess-open.md).</span><span class="sxs-lookup"><span data-stu-id="9eb70-125">To open a file, call [**Open**](iscardfileaccess-open.md).</span></span>

<span data-ttu-id="9eb70-126">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="9eb70-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="9eb70-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9eb70-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9eb70-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9eb70-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb70-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb70-129">Requirements</span></span>



| <span data-ttu-id="9eb70-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb70-130">Requirement</span></span> | <span data-ttu-id="9eb70-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb70-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9eb70-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb70-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb70-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9eb70-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb70-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb70-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9eb70-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9eb70-136">End of client support</span></span><br/>    | <span data-ttu-id="9eb70-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9eb70-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9eb70-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9eb70-138">End of server support</span></span><br/>    | <span data-ttu-id="9eb70-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9eb70-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9eb70-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eb70-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb70-141">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="9eb70-141">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="9eb70-142">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="9eb70-142">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
