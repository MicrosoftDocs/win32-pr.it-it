---
description: Imposta una nuova parola di stato del messaggio APDU di risposta.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: 'ISCardCmd: metodo:p ut_ReplyStatus (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128298"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="813fa-103">ISCardCmd::p UT \_ ReplyStatus metodo</span><span class="sxs-lookup"><span data-stu-id="813fa-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="813fa-104">\[Il metodo **put \_ ReplyStatus** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="813fa-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="813fa-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="813fa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="813fa-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="813fa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="813fa-107">Il metodo **put \_ ReplyStatus** imposta una nuova parola di stato del messaggio [*APDU di risposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="813fa-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="813fa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="813fa-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="813fa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="813fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="813fa-110">*wStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="813fa-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="813fa-111">Parola che rappresenta lo stato.</span><span class="sxs-lookup"><span data-stu-id="813fa-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="813fa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="813fa-112">Return value</span></span>

<span data-ttu-id="813fa-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="813fa-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="813fa-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="813fa-114">Return code</span></span>                                                                                   | <span data-ttu-id="813fa-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="813fa-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="813fa-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="813fa-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="813fa-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="813fa-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="813fa-119">Il parametro *wStatus* non è valido.</span><span class="sxs-lookup"><span data-stu-id="813fa-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="813fa-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="813fa-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="813fa-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="813fa-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="813fa-122">Remarks</span></span>

<span data-ttu-id="813fa-123">Per ottenere la parola di stato del messaggio di APDU di risposta, chiamare [**get \_ ReplyStatus**](iscardcmd-get-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="813fa-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="813fa-124">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="813fa-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="813fa-125">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="813fa-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="813fa-126">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="813fa-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="813fa-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="813fa-127">Examples</span></span>

<span data-ttu-id="813fa-128">Nell'esempio seguente viene illustrato come impostare una nuova parola di stato del messaggio [*APDU di risposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="813fa-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="813fa-129">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="813fa-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="813fa-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="813fa-130">Requirements</span></span>



| <span data-ttu-id="813fa-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="813fa-131">Requirement</span></span> | <span data-ttu-id="813fa-132">Valore</span><span class="sxs-lookup"><span data-stu-id="813fa-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="813fa-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="813fa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="813fa-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="813fa-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="813fa-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="813fa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="813fa-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="813fa-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="813fa-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="813fa-137">End of client support</span></span><br/>    | <span data-ttu-id="813fa-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="813fa-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="813fa-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="813fa-139">End of server support</span></span><br/>    | <span data-ttu-id="813fa-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="813fa-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="813fa-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="813fa-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="813fa-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="813fa-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="813fa-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="813fa-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="813fa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="813fa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="813fa-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="813fa-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="813fa-147">IID</span><span class="sxs-lookup"><span data-stu-id="813fa-147">IID</span></span><br/>                      | <span data-ttu-id="813fa-148">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="813fa-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="813fa-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="813fa-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813fa-150">**ottenere \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="813fa-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="813fa-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="813fa-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
