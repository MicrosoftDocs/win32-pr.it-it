---
description: Il metodo Create crea un file in una posizione specifica all'interno della smart card file system.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'Metodo ISCardFileAccess:: create'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129318"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="b303a-103">Metodo ISCardFileAccess:: create</span><span class="sxs-lookup"><span data-stu-id="b303a-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="b303a-104">\[Il metodo **create** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b303a-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b303a-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b303a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b303a-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="b303a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b303a-107">Il metodo **create** crea un file in una posizione specifica all'interno della [*Smart Card*](../secgloss/s-gly.md) file System.</span><span class="sxs-lookup"><span data-stu-id="b303a-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b303a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b303a-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b303a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b303a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b303a-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b303a-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b303a-111">Tipo di riferimento usato in *bstrPathSpec*.</span><span class="sxs-lookup"><span data-stu-id="b303a-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="b303a-112">**\_tipo SC \_ per \_ nome**</span><span class="sxs-lookup"><span data-stu-id="b303a-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="b303a-113">**\_tipo SC \_ per \_ ID**</span><span class="sxs-lookup"><span data-stu-id="b303a-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="b303a-114">**\_tipo SC \_ per \_ breve**</span><span class="sxs-lookup"><span data-stu-id="b303a-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="b303a-115">**SC \_ digitare \_ per \_ qualsiasi**</span><span class="sxs-lookup"><span data-stu-id="b303a-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b303a-116">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b303a-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b303a-117">ID file da creare nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="b303a-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="b303a-118">*TLV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b303a-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b303a-119">Elenco di strutture TLV (tag, lunghezza, valore) per cui è necessario impostare i valori.</span><span class="sxs-lookup"><span data-stu-id="b303a-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b303a-120">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b303a-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b303a-121">Specifica se è necessario utilizzare la messaggistica protetta e i dati preallocati.</span><span class="sxs-lookup"><span data-stu-id="b303a-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="b303a-122">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="b303a-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="b303a-123">**SC \_ FL \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="b303a-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b303a-124">*pDataBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b303a-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b303a-125">Puntatore ai dati preallocati.</span><span class="sxs-lookup"><span data-stu-id="b303a-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b303a-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b303a-126">Return value</span></span>

<span data-ttu-id="b303a-127">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="b303a-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b303a-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b303a-128">Return code</span></span>                                                                                   | <span data-ttu-id="b303a-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b303a-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b303a-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b303a-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b303a-131">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b303a-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b303a-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b303a-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b303a-133">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="b303a-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b303a-134"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b303a-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b303a-135">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="b303a-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b303a-136"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="b303a-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b303a-137">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b303a-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b303a-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="b303a-138">Remarks</span></span>

<span data-ttu-id="b303a-139">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="b303a-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b303a-140">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="b303a-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b303a-141">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b303a-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b303a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b303a-142">Requirements</span></span>



| <span data-ttu-id="b303a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b303a-143">Requirement</span></span> | <span data-ttu-id="b303a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b303a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b303a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b303a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b303a-146">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b303a-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b303a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b303a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b303a-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b303a-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b303a-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b303a-149">End of client support</span></span><br/>    | <span data-ttu-id="b303a-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b303a-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b303a-151">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b303a-151">End of server support</span></span><br/>    | <span data-ttu-id="b303a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b303a-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b303a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b303a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b303a-154">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="b303a-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
