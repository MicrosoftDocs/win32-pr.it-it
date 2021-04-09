---
description: Il metodo Write scrive i dati in un file aperto corrente.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'Metodo ISCardFileAccess:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131454"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="9a156-103">Metodo ISCardFileAccess:: Write</span><span class="sxs-lookup"><span data-stu-id="9a156-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="9a156-104">\[Il metodo **Write** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9a156-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9a156-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a156-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a156-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9a156-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9a156-107">Il metodo **Write** scrive i dati in un file aperto corrente.</span><span class="sxs-lookup"><span data-stu-id="9a156-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a156-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a156-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="9a156-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a156-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a156-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a156-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a156-111">Handle per un file aperto.</span><span class="sxs-lookup"><span data-stu-id="9a156-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="9a156-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a156-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a156-113">Oggetto/dati da scrivere.</span><span class="sxs-lookup"><span data-stu-id="9a156-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="9a156-114">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a156-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a156-115">Specifica se utilizzare la messaggistica protetta.</span><span class="sxs-lookup"><span data-stu-id="9a156-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="9a156-116">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="9a156-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a156-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a156-117">Return value</span></span>

<span data-ttu-id="9a156-118">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a156-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9a156-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9a156-119">Return code</span></span>                                                                                   | <span data-ttu-id="9a156-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a156-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9a156-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a156-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9a156-122">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9a156-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9a156-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9a156-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9a156-124">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="9a156-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9a156-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a156-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9a156-126">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="9a156-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9a156-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9a156-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9a156-128">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9a156-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9a156-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a156-129">Remarks</span></span>

<span data-ttu-id="9a156-130">Per aprire o chiudere un file, chiamare rispettivamente [**Open**](iscardfileaccess-open.md) o [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="9a156-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="9a156-131">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="9a156-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="9a156-132">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9a156-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9a156-133">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9a156-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a156-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a156-134">Requirements</span></span>



| <span data-ttu-id="9a156-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a156-135">Requirement</span></span> | <span data-ttu-id="9a156-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9a156-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9a156-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a156-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9a156-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9a156-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9a156-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a156-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9a156-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a156-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9a156-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9a156-141">End of client support</span></span><br/>    | <span data-ttu-id="9a156-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a156-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9a156-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9a156-143">End of server support</span></span><br/>    | <span data-ttu-id="9a156-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a156-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9a156-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a156-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a156-146">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="9a156-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="9a156-147">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="9a156-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="9a156-148">**Aprire**</span><span class="sxs-lookup"><span data-stu-id="9a156-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
