---
description: Il metodo ListReaders recupera i nomi dei lettori di smart card registrati nel database delle smart card.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'Metodo ISCardDatabase:: ListReaders (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307235"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="408f0-103">Metodo ISCardDatabase:: ListReaders</span><span class="sxs-lookup"><span data-stu-id="408f0-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="408f0-104">\[Il metodo **ListReaders** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="408f0-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="408f0-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="408f0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="408f0-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="408f0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="408f0-107">Il metodo **ListReaders** recupera i nomi dei [*lettori*](../secgloss/r-gly.md) di smart card registrati nel [*database delle smart card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="408f0-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="408f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="408f0-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="408f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="408f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408f0-110">*LocaleID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408f0-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408f0-111">ID localizzazione della lingua.</span><span class="sxs-lookup"><span data-stu-id="408f0-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="408f0-112">*ppReaders* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="408f0-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="408f0-113">Puntatore a un SAFEARRAY di BSTR che contiene i nomi dei lettori della smart card, in caso di esito positivo; **Null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="408f0-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="408f0-114">Return value</span></span>

<span data-ttu-id="408f0-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="408f0-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="408f0-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="408f0-116">Return code</span></span>                                                                                   | <span data-ttu-id="408f0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="408f0-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="408f0-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="408f0-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="408f0-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="408f0-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="408f0-121">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="408f0-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="408f0-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="408f0-123">Un puntatore errato è stato passato in *ppReaders*.</span><span class="sxs-lookup"><span data-stu-id="408f0-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="408f0-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="408f0-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="408f0-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="408f0-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="408f0-126">Remarks</span></span>

<span data-ttu-id="408f0-127">Per recuperare tutti i gruppi di [*Smart Card*](../secgloss/s-gly.md) o [*Reader*](../secgloss/r-gly.md)noti, chiamare rispettivamente [**ListCards**](iscarddatabase-listcards.md) o [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="408f0-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="408f0-128">Per recuperare rispettivamente il [*provider di servizi primario*](../secgloss/p-gly.md) o le interfacce di una scheda specifica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="408f0-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="408f0-129">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="408f0-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="408f0-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="408f0-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="408f0-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="408f0-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="408f0-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="408f0-132">Examples</span></span>

<span data-ttu-id="408f0-133">Nell'esempio seguente viene illustrato come recuperare i nomi dei lettori di smart card registrati nel database delle smart card.</span><span class="sxs-lookup"><span data-stu-id="408f0-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="408f0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="408f0-134">Requirements</span></span>



| <span data-ttu-id="408f0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="408f0-135">Requirement</span></span> | <span data-ttu-id="408f0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="408f0-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="408f0-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="408f0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="408f0-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="408f0-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="408f0-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="408f0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="408f0-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="408f0-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="408f0-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="408f0-141">End of client support</span></span><br/>    | <span data-ttu-id="408f0-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="408f0-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="408f0-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="408f0-143">End of server support</span></span><br/>    | <span data-ttu-id="408f0-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="408f0-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="408f0-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="408f0-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="408f0-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="408f0-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="408f0-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="408f0-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="408f0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="408f0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408f0-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408f0-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="408f0-151">IID</span><span class="sxs-lookup"><span data-stu-id="408f0-151">IID</span></span><br/>                      | <span data-ttu-id="408f0-152">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="408f0-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="408f0-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="408f0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408f0-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="408f0-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="408f0-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="408f0-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="408f0-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="408f0-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="408f0-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="408f0-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="408f0-158">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="408f0-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
