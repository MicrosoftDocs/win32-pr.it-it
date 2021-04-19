---
description: Il metodo FindCard cerca la smart card e apre una connessione valida.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Metodo ISCardLocate:: FindCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311617"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="6472b-103">Metodo ISCardLocate:: FindCard</span><span class="sxs-lookup"><span data-stu-id="6472b-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="6472b-104">\[Il metodo **FindCard** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="6472b-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6472b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6472b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6472b-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="6472b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6472b-107">Il metodo **FindCard** cerca la [*Smart Card*](../secgloss/s-gly.md) e apre una connessione valida.</span><span class="sxs-lookup"><span data-stu-id="6472b-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="6472b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6472b-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6472b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6472b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6472b-110">*SHAREMODE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6472b-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472b-111">Modalità in cui condividere o non condividere la smart card quando viene aperta una connessione.</span><span class="sxs-lookup"><span data-stu-id="6472b-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="6472b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="6472b-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="6472b-113">Significato</span><span class="sxs-lookup"><span data-stu-id="6472b-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="6472b-114"><dt>**ESCLUSIVO**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="6472b-115">Nessun altro usa questa connessione alla smart card.</span><span class="sxs-lookup"><span data-stu-id="6472b-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="6472b-116"><dt>**CONDIVISO**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="6472b-117">Questa connessione può essere utilizzata da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6472b-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="6472b-118">*Protocolli* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6472b-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472b-119">Protocollo da usare per la connessione alla scheda.</span><span class="sxs-lookup"><span data-stu-id="6472b-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="6472b-120">T0</span><span class="sxs-lookup"><span data-stu-id="6472b-120">T0</span></span>

<span data-ttu-id="6472b-121">T1</span><span class="sxs-lookup"><span data-stu-id="6472b-121">T1</span></span>

<span data-ttu-id="6472b-122">RAW</span><span class="sxs-lookup"><span data-stu-id="6472b-122">RAW</span></span>

<span data-ttu-id="6472b-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="6472b-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="6472b-124">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6472b-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6472b-125">Specifica quando viene visualizzata l' [*interfaccia utente*](../secgloss/u-gly.md) :</span><span class="sxs-lookup"><span data-stu-id="6472b-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="6472b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6472b-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="6472b-127">Significato</span><span class="sxs-lookup"><span data-stu-id="6472b-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="6472b-128"><dt>**\_ \_ interfaccia utente minima di SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="6472b-129">Visualizza la finestra di dialogo solo se la scheda cercata dall'applicazione chiamante non si trova e non è disponibile per l'utilizzo in un lettore.</span><span class="sxs-lookup"><span data-stu-id="6472b-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="6472b-130">Ciò consente di trovare la scheda, connessa (tramite un meccanismo interno della finestra di dialogo o usando le funzioni di callback utente) e restituita all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="6472b-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="6472b-131"><dt>**SC \_ DLG \_ Nessuna \_ interfaccia utente**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="6472b-132">Non comporta la visualizzazione dell'interfaccia utente, indipendentemente dal risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="6472b-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="6472b-133"><dt>**\_ \_ interfaccia utente Force SC DLG \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="6472b-134">Causa la visualizzazione dell'interfaccia utente indipendentemente dal risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="6472b-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="6472b-135">*ppCardInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6472b-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6472b-136">Puntatore a un puntatore a una struttura di dati che contiene o restituisce informazioni sulla [*Smart Card*](../secgloss/s-gly.md)aperta, in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6472b-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="6472b-137">Sarà **null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6472b-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6472b-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6472b-138">Return value</span></span>

<span data-ttu-id="6472b-139">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="6472b-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6472b-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6472b-140">Return code</span></span>                                                                                   | <span data-ttu-id="6472b-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6472b-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6472b-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6472b-143">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="6472b-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="6472b-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6472b-145">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="6472b-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="6472b-146"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6472b-147">Un puntatore errato è stato passato in *ppCardInfo*.</span><span class="sxs-lookup"><span data-stu-id="6472b-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="6472b-148"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6472b-149">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="6472b-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="6472b-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="6472b-150">Remarks</span></span>

<span data-ttu-id="6472b-151">Per impostare i criteri di ricerca della ricerca, chiamare [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) per specificare i nomi delle schede della smart card.</span><span class="sxs-lookup"><span data-stu-id="6472b-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="6472b-152">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardLocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="6472b-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="6472b-153">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6472b-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6472b-154">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6472b-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6472b-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6472b-155">Requirements</span></span>



| <span data-ttu-id="6472b-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="6472b-156">Requirement</span></span> | <span data-ttu-id="6472b-157">Valore</span><span class="sxs-lookup"><span data-stu-id="6472b-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6472b-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6472b-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6472b-159">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6472b-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6472b-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6472b-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6472b-161">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6472b-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6472b-162">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6472b-162">End of client support</span></span><br/>    | <span data-ttu-id="6472b-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6472b-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6472b-164">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6472b-164">End of server support</span></span><br/>    | <span data-ttu-id="6472b-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6472b-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6472b-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6472b-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="6472b-167"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6472b-168">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6472b-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="6472b-169"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6472b-170">DLL</span><span class="sxs-lookup"><span data-stu-id="6472b-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6472b-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6472b-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6472b-172">IID</span><span class="sxs-lookup"><span data-stu-id="6472b-172">IID</span></span><br/>                      | <span data-ttu-id="6472b-173">IID \_ ISCardLocate è definito come 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6472b-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="6472b-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6472b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6472b-175">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="6472b-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="6472b-176">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="6472b-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
