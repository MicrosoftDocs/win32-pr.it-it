---
description: Il metodo ListReaderGroups recupera i nomi dei gruppi di Reader registrati nel database delle smart card.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'Metodo ISCardDatabase:: ListReaderGroups (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129326"
---
# <a name="iscarddatabaselistreadergroups-method"></a><span data-ttu-id="f542e-103">Metodo ISCardDatabase:: ListReaderGroups</span><span class="sxs-lookup"><span data-stu-id="f542e-103">ISCardDatabase::ListReaderGroups method</span></span>

<span data-ttu-id="f542e-104">\[Il metodo **ListReaderGroups** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f542e-104">\[The **ListReaderGroups** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f542e-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f542e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f542e-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f542e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f542e-107">Il metodo **ListReaderGroups** recupera i nomi dei [*gruppi di Reader*](../secgloss/r-gly.md) registrati nel database delle smart card.</span><span class="sxs-lookup"><span data-stu-id="f542e-107">The **ListReaderGroups** method retrieves the names of the [*reader groups*](../secgloss/r-gly.md) registered in the smart card database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f542e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f542e-108">Syntax</span></span>


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a><span data-ttu-id="f542e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f542e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f542e-110">*LocaleID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f542e-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f542e-111">ID localizzazione della lingua.</span><span class="sxs-lookup"><span data-stu-id="f542e-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="f542e-112">*ppReaderGroups* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f542e-112">*ppReaderGroups* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f542e-113">Puntatore a un SAFEARRAY di BSTR che contiene i nomi dei gruppi di lettori di smart card che soddisfano i parametri di ricerca in caso di esito positivo; **Null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f542e-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card reader groups that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f542e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f542e-114">Return value</span></span>

<span data-ttu-id="f542e-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="f542e-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f542e-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f542e-116">Return code</span></span>                                                                                   | <span data-ttu-id="f542e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f542e-117">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f542e-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f542e-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f542e-119">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="f542e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f542e-121">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="f542e-121">Invalid parameter.</span></span><br/>                            |
| <dl> <span data-ttu-id="f542e-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f542e-123">Un puntatore errato è stato passato in *ppReaderGroups*.</span><span class="sxs-lookup"><span data-stu-id="f542e-123">A bad pointer was passed in *ppReaderGroups*.</span></span><br/> |
| <dl> <span data-ttu-id="f542e-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f542e-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f542e-125">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="f542e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="f542e-126">Remarks</span></span>

<span data-ttu-id="f542e-127">Per recuperare tutte le [*Smart Card*](../secgloss/s-gly.md) o i [*lettori*](../secgloss/r-gly.md)noti, chiamare rispettivamente [**ListCards**](iscarddatabase-listcards.md) o [**ListReaders**](iscarddatabase-listreaders.md) .</span><span class="sxs-lookup"><span data-stu-id="f542e-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*readers*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaders**](iscarddatabase-listreaders.md) respectively.</span></span>

<span data-ttu-id="f542e-128">Per recuperare rispettivamente il [*provider di servizi primario*](../secgloss/p-gly.md) o le interfacce di una scheda specifica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="f542e-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="f542e-129">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="f542e-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="f542e-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="f542e-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f542e-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f542e-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f542e-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="f542e-132">Examples</span></span>

<span data-ttu-id="f542e-133">Nell'esempio seguente viene illustrato come recuperare i nomi dei gruppi di Reader registrati nel database delle smart card.</span><span class="sxs-lookup"><span data-stu-id="f542e-133">The following example shows retrieving the names of the reader groups registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="f542e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f542e-134">Requirements</span></span>



| <span data-ttu-id="f542e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f542e-135">Requirement</span></span> | <span data-ttu-id="f542e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f542e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f542e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f542e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f542e-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f542e-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f542e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f542e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f542e-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f542e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f542e-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f542e-141">End of client support</span></span><br/>    | <span data-ttu-id="f542e-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f542e-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f542e-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f542e-143">End of server support</span></span><br/>    | <span data-ttu-id="f542e-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f542e-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f542e-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f542e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f542e-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="f542e-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f542e-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="f542e-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f542e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f542e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f542e-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f542e-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f542e-151">IID</span><span class="sxs-lookup"><span data-stu-id="f542e-151">IID</span></span><br/>                      | <span data-ttu-id="f542e-152">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f542e-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f542e-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f542e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f542e-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="f542e-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="f542e-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="f542e-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="f542e-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="f542e-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="f542e-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="f542e-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="f542e-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="f542e-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
