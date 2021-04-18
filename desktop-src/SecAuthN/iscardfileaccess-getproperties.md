---
description: Recupera i dati primitivi a cui fa riferimento TLVs (tag, lunghezza, valore) per l'oggetto specificato.
ms.assetid: 135aeb9a-b851-4522-862f-02a7e020c36b
title: 'Metodo ISCardFileAccess:: GetProperties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 25e6ae1ab657d92dda0ad421b650eaaa7076bd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314171"
---
# <a name="iscardfileaccessgetproperties-method"></a><span data-ttu-id="f1ba4-103">Metodo ISCardFileAccess:: GetProperties</span><span class="sxs-lookup"><span data-stu-id="f1ba4-103">ISCardFileAccess::GetProperties method</span></span>

<span data-ttu-id="f1ba4-104">\[Il metodo **GetProperties** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-104">\[The **GetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f1ba4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1ba4-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f1ba4-107">Il metodo **GetProperties** recupera i dati primitivi a cui fa riferimento TLVs (tag, length, value) per l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-107">The **GetProperties** method retrieves the primitive data referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ba4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1ba4-108">Syntax</span></span>


```C++
HRESULT GetProperties(
  [in]      REFTYPE     refType,
  [in]      BSTR        bstrPathSpec,
  [in]      SCARD_FLAGS flags,
  [in, out] LPTLV_TABLE *ppTLV
);
```



## <a name="parameters"></a><span data-ttu-id="f1ba4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1ba4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ba4-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ba4-111">Tipo di riferimento usato in *bstrNewDir*.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-111">Type of reference used in *bstrNewDir*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="f1ba4-112">**\_tipo SC \_ per \_ nome**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="f1ba4-113">**\_tipo SC \_ per \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="f1ba4-114">**\_tipo SC \_ per \_ breve**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="f1ba4-115">**SC \_ digitare \_ per \_ qualsiasi**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f1ba4-116">*bstrPathSpec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ba4-117">File.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="f1ba4-118">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ba4-119">Specifica se utilizzare la messaggistica protetta.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="f1ba4-120">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f1ba4-121">*ppTLV* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-121">*ppTLV* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ba4-122">Puntatore a strutture TLV il cui valore è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-122">Pointer to TLV structures whose value has been retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ba4-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1ba4-123">Return value</span></span>

<span data-ttu-id="f1ba4-124">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f1ba4-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1ba4-125">Return code</span></span>                                                                                   | <span data-ttu-id="f1ba4-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ba4-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f1ba4-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ba4-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1ba4-128">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f1ba4-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ba4-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f1ba4-130">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f1ba4-131"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ba4-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f1ba4-132">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f1ba4-133"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ba4-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1ba4-134">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f1ba4-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1ba4-135">Remarks</span></span>

<span data-ttu-id="f1ba4-136">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="f1ba4-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="f1ba4-137">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="f1ba4-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f1ba4-138">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f1ba4-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ba4-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1ba4-139">Requirements</span></span>



| <span data-ttu-id="f1ba4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ba4-140">Requirement</span></span> | <span data-ttu-id="f1ba4-141">Valore</span><span class="sxs-lookup"><span data-stu-id="f1ba4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1ba4-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1ba4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ba4-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f1ba4-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1ba4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ba4-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1ba4-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1ba4-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f1ba4-146">End of client support</span></span><br/>    | <span data-ttu-id="f1ba4-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1ba4-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f1ba4-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f1ba4-148">End of server support</span></span><br/>    | <span data-ttu-id="f1ba4-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1ba4-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="f1ba4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1ba4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ba4-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="f1ba4-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
