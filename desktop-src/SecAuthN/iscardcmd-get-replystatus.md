---
description: Recupera la parola di stato del messaggio di APDU di risposta.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Metodo ISCardCmd:: get_ReplyStatus (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129334"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="21bd6-103">Metodo ISCardCmd:: Get \_ ReplyStatus</span><span class="sxs-lookup"><span data-stu-id="21bd6-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="21bd6-104">\[Il metodo **get \_ ReplyStatus** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="21bd6-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21bd6-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21bd6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="21bd6-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="21bd6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="21bd6-107">Il metodo **get \_ ReplyStatus** recupera la parola di stato del messaggio [*di APDU Reply*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="21bd6-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bd6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21bd6-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="21bd6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21bd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bd6-110">*pwStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="21bd6-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21bd6-111">Puntatore alla parola che corrisponde allo stato restituito.</span><span class="sxs-lookup"><span data-stu-id="21bd6-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bd6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21bd6-112">Return value</span></span>

<span data-ttu-id="21bd6-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="21bd6-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="21bd6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="21bd6-114">Return code</span></span>                                                                                   | <span data-ttu-id="21bd6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21bd6-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="21bd6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="21bd6-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="21bd6-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="21bd6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="21bd6-119">Il parametro *pwStatus* non è valido.</span><span class="sxs-lookup"><span data-stu-id="21bd6-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="21bd6-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="21bd6-121">Un puntatore errato è stato passato in *pwStatus*.</span><span class="sxs-lookup"><span data-stu-id="21bd6-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="21bd6-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="21bd6-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="21bd6-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="21bd6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="21bd6-124">Remarks</span></span>

<span data-ttu-id="21bd6-125">Per impostare la parola di stato del messaggio di APDU di risposta, chiamare [**put \_ ReplyStatus**](iscardcmd-put-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="21bd6-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="21bd6-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="21bd6-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="21bd6-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="21bd6-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="21bd6-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="21bd6-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="21bd6-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="21bd6-129">Examples</span></span>

<span data-ttu-id="21bd6-130">Nell'esempio seguente viene illustrato come recuperare la parola di stato del messaggio del [*APDU di risposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="21bd6-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="21bd6-131">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="21bd6-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="21bd6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21bd6-132">Requirements</span></span>



| <span data-ttu-id="21bd6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="21bd6-133">Requirement</span></span> | <span data-ttu-id="21bd6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="21bd6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21bd6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21bd6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="21bd6-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="21bd6-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="21bd6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21bd6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="21bd6-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21bd6-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21bd6-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="21bd6-139">End of client support</span></span><br/>    | <span data-ttu-id="21bd6-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21bd6-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="21bd6-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="21bd6-141">End of server support</span></span><br/>    | <span data-ttu-id="21bd6-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21bd6-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="21bd6-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21bd6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="21bd6-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="21bd6-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="21bd6-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="21bd6-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21bd6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="21bd6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21bd6-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21bd6-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21bd6-149">IID</span><span class="sxs-lookup"><span data-stu-id="21bd6-149">IID</span></span><br/>                      | <span data-ttu-id="21bd6-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="21bd6-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="21bd6-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21bd6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bd6-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="21bd6-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="21bd6-153">**Inserisci \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="21bd6-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
