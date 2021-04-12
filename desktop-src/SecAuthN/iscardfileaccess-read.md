---
description: Il metodo Read legge e restituisce i dati specificati da un file specificato.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'Metodo ISCardFileAccess:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231717"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="a6db6-103">Metodo ISCardFileAccess:: Read</span><span class="sxs-lookup"><span data-stu-id="a6db6-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="a6db6-104">\[Il metodo **Read** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a6db6-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a6db6-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a6db6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a6db6-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a6db6-107">Il metodo **Read** legge e restituisce i dati specificati da un file specificato.</span><span class="sxs-lookup"><span data-stu-id="a6db6-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6db6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6db6-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a6db6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6db6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6db6-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6db6-111">Handle del file aperto a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="a6db6-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="a6db6-112">*lBytesToRead* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6db6-113">Lunghezza dei dati da leggere (in) o numero di byte letti (out).</span><span class="sxs-lookup"><span data-stu-id="a6db6-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="a6db6-114">Restituisce l'elenco di file come matrice di BSTR.</span><span class="sxs-lookup"><span data-stu-id="a6db6-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="a6db6-115">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6db6-116">Specifica se utilizzare la messaggistica protetta.</span><span class="sxs-lookup"><span data-stu-id="a6db6-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="a6db6-117">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="a6db6-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a6db6-118">*ppBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6db6-119">Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i dati letti.</span><span class="sxs-lookup"><span data-stu-id="a6db6-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6db6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6db6-120">Return value</span></span>

<span data-ttu-id="a6db6-121">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6db6-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a6db6-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a6db6-122">Return code</span></span>                                                                                   | <span data-ttu-id="a6db6-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6db6-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a6db6-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6db6-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a6db6-125">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a6db6-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a6db6-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a6db6-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a6db6-127">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a6db6-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a6db6-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6db6-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a6db6-129">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="a6db6-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a6db6-130"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a6db6-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a6db6-131">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a6db6-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a6db6-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6db6-132">Remarks</span></span>

<span data-ttu-id="a6db6-133">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="a6db6-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="a6db6-134">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a6db6-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a6db6-135">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a6db6-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6db6-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6db6-136">Requirements</span></span>



| <span data-ttu-id="a6db6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6db6-137">Requirement</span></span> | <span data-ttu-id="a6db6-138">Valore</span><span class="sxs-lookup"><span data-stu-id="a6db6-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6db6-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6db6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a6db6-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a6db6-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6db6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a6db6-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6db6-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a6db6-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a6db6-143">End of client support</span></span><br/>    | <span data-ttu-id="a6db6-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6db6-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a6db6-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a6db6-145">End of server support</span></span><br/>    | <span data-ttu-id="a6db6-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a6db6-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a6db6-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6db6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6db6-148">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="a6db6-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
