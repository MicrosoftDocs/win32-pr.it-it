---
description: Il metodo ConfigureCardNameSearch specifica i nomi delle schede da usare nella ricerca della smart card.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Metodo ISCardLocate:: ConfigureCardNameSearch (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232038"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="5122f-103">Metodo ISCardLocate:: ConfigureCardNameSearch</span><span class="sxs-lookup"><span data-stu-id="5122f-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="5122f-104">\[Il metodo **ConfigureCardNameSearch** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5122f-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5122f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5122f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5122f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5122f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5122f-107">Il metodo **ConfigureCardNameSearch** specifica i nomi delle schede da usare nella ricerca della [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5122f-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5122f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5122f-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5122f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5122f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5122f-110">*pCardNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5122f-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5122f-111">Puntatore a una matrice di nomi di schede sicura di automazione in formato BSTR.</span><span class="sxs-lookup"><span data-stu-id="5122f-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-112">*pGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5122f-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5122f-113">Puntatore a una matrice sicura di automazione dei nomi dei gruppi di schede/Reader nel formato BSTR da aggiungere alla ricerca.</span><span class="sxs-lookup"><span data-stu-id="5122f-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-114">*bstrTitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5122f-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5122f-115">Titolo della finestra di dialogo per il controllo comune di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5122f-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="5122f-116">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5122f-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5122f-117">Specifica quando viene visualizzata l' [*interfaccia utente*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5122f-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="5122f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5122f-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="5122f-119">Significato</span><span class="sxs-lookup"><span data-stu-id="5122f-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="5122f-120"><dt>**\_ \_ interfaccia utente minima di SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="5122f-121">Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non si trova e non è disponibile per l'utilizzo in un lettore.</span><span class="sxs-lookup"><span data-stu-id="5122f-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="5122f-122">Ciò consente di trovare la scheda, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback utente) e restituita all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="5122f-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="5122f-123"><dt>**SC \_ DLG \_ Nessuna \_ interfaccia utente**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="5122f-124">Non comporta la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="5122f-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="5122f-125"><dt>**\_ \_ interfaccia utente Force SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="5122f-126">Causa la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="5122f-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5122f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5122f-127">Return value</span></span>

<span data-ttu-id="5122f-128">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="5122f-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5122f-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5122f-129">Return code</span></span>                                                                                   | <span data-ttu-id="5122f-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5122f-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5122f-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5122f-132">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="5122f-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="5122f-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5122f-134">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="5122f-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5122f-135"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5122f-136">Un puntatore errato è stato passato in *pCardNames* o *pGroupNames*.</span><span class="sxs-lookup"><span data-stu-id="5122f-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="5122f-137"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5122f-138">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="5122f-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5122f-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="5122f-139">Remarks</span></span>

<span data-ttu-id="5122f-140">Per individuare la [*Smart Card*](../secgloss/s-gly.md), chiamare [**FindCard**](iscardlocate-findcard.md).</span><span class="sxs-lookup"><span data-stu-id="5122f-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="5122f-141">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="5122f-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="5122f-142">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5122f-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5122f-143">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5122f-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5122f-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5122f-144">Requirements</span></span>



| <span data-ttu-id="5122f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5122f-145">Requirement</span></span> | <span data-ttu-id="5122f-146">Valore</span><span class="sxs-lookup"><span data-stu-id="5122f-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5122f-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5122f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="5122f-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5122f-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5122f-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5122f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="5122f-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5122f-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5122f-151">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5122f-151">End of client support</span></span><br/>    | <span data-ttu-id="5122f-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5122f-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5122f-153">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5122f-153">End of server support</span></span><br/>    | <span data-ttu-id="5122f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5122f-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5122f-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5122f-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="5122f-156"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="5122f-157">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5122f-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="5122f-158"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5122f-159">DLL</span><span class="sxs-lookup"><span data-stu-id="5122f-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5122f-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5122f-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5122f-161">IID</span><span class="sxs-lookup"><span data-stu-id="5122f-161">IID</span></span><br/>                      | <span data-ttu-id="5122f-162">IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5122f-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5122f-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5122f-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5122f-164">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="5122f-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="5122f-165">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="5122f-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
