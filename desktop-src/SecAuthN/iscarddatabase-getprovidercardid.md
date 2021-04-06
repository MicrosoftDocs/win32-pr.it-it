---
description: Il metodo GetProviderCardId recupera l'identificatore (GUID) del provider di servizi primario per la smart card specificata.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Metodo ISCardDatabase:: GetProviderCardId (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758825"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="58723-103">Metodo ISCardDatabase:: GetProviderCardId</span><span class="sxs-lookup"><span data-stu-id="58723-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="58723-104">\[Il metodo **GetProviderCardId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="58723-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58723-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="58723-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="58723-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="58723-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="58723-107">Il metodo **GetProviderCardId** recupera l'identificatore (Guid) del [*provider di servizi primario*](../secgloss/p-gly.md) per la [*Smart Card*](../secgloss/s-gly.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="58723-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="58723-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58723-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="58723-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="58723-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58723-110">*bstrCardName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58723-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58723-111">Nome della smart card.</span><span class="sxs-lookup"><span data-stu-id="58723-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="58723-112">*ppguidProviderId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58723-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58723-113">Puntatore all'identificatore (GUID) del provider di servizi primario in caso di esito positivo; **Null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="58723-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58723-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58723-114">Return value</span></span>

<span data-ttu-id="58723-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="58723-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="58723-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="58723-116">Return code</span></span>                                                                                   | <span data-ttu-id="58723-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58723-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="58723-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="58723-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="58723-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="58723-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="58723-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58723-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="58723-121">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="58723-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="58723-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="58723-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="58723-123">Un puntatore errato è stato passato in *ppguidProviderId*.</span><span class="sxs-lookup"><span data-stu-id="58723-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="58723-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="58723-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="58723-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="58723-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="58723-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="58723-126">Remarks</span></span>

<span data-ttu-id="58723-127">Per elencare le interfacce della smart card, chiamare [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span><span class="sxs-lookup"><span data-stu-id="58723-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="58723-128">Per recuperare tutte le [*Smart Card*](../secgloss/s-gly.md), [*i reader e*](../secgloss/r-gly.md) i [*gruppi di Reader*](../secgloss/r-gly.md) noti, chiamare rispettivamente [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="58723-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="58723-129">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="58723-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="58723-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="58723-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="58723-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="58723-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="58723-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="58723-132">Examples</span></span>

<span data-ttu-id="58723-133">Nell'esempio seguente viene illustrato come recuperare l'identificatore del provider di servizi primario per la smart card specificata.</span><span class="sxs-lookup"><span data-stu-id="58723-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="58723-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58723-134">Requirements</span></span>



| <span data-ttu-id="58723-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="58723-135">Requirement</span></span> | <span data-ttu-id="58723-136">Valore</span><span class="sxs-lookup"><span data-stu-id="58723-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58723-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58723-137">Minimum supported client</span></span><br/> | <span data-ttu-id="58723-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58723-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="58723-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58723-139">Minimum supported server</span></span><br/> | <span data-ttu-id="58723-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58723-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58723-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="58723-141">End of client support</span></span><br/>    | <span data-ttu-id="58723-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="58723-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="58723-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="58723-143">End of server support</span></span><br/>    | <span data-ttu-id="58723-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58723-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="58723-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58723-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="58723-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="58723-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="58723-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="58723-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="58723-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58723-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58723-149">DLL</span><span class="sxs-lookup"><span data-stu-id="58723-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58723-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58723-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="58723-151">IID</span><span class="sxs-lookup"><span data-stu-id="58723-151">IID</span></span><br/>                      | <span data-ttu-id="58723-152">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="58723-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="58723-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58723-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58723-154">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="58723-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="58723-155">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="58723-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="58723-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="58723-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="58723-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="58723-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="58723-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="58723-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
