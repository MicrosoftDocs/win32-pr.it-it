---
description: Recupera il byte di stato APDU SW2 di risposta.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'Metodo ISCardCmd:: get_ReplyStatusSW2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129331"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="d3d26-103">Metodo ISCardCmd:: Get \_ ReplyStatusSW2</span><span class="sxs-lookup"><span data-stu-id="d3d26-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="d3d26-104">\[Il metodo **get \_ ReplyStatusSW2** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d3d26-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d3d26-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d3d26-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d3d26-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d3d26-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d3d26-107">Il metodo **get \_ ReplyStatusSW2** Recupera il byte di stato della [*risposta APDU*](../secgloss/r-gly.md) SW2.</span><span class="sxs-lookup"><span data-stu-id="d3d26-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d26-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3d26-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="d3d26-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3d26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d26-110">*pbySW2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3d26-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d26-111">Puntatore al byte che contiene il valore del byte SW2 al ritorno.</span><span class="sxs-lookup"><span data-stu-id="d3d26-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d26-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3d26-112">Return value</span></span>

<span data-ttu-id="d3d26-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3d26-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d3d26-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d3d26-114">Return code</span></span>                                                                                   | <span data-ttu-id="d3d26-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d26-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d3d26-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d3d26-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d3d26-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d3d26-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d3d26-119">*PbySW2* non valido.</span><span class="sxs-lookup"><span data-stu-id="d3d26-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="d3d26-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d3d26-121">Un puntatore errato è stato passato in *pbySW2*.</span><span class="sxs-lookup"><span data-stu-id="d3d26-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="d3d26-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d3d26-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="d3d26-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d3d26-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3d26-124">Remarks</span></span>

<span data-ttu-id="d3d26-125">Il byte di stato SW2 di APDU di risposta è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d3d26-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="d3d26-126">Per recuperare il byte di stato SW1 di APDU di risposta, chiamare [**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span><span class="sxs-lookup"><span data-stu-id="d3d26-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="d3d26-127">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="d3d26-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d3d26-128">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d3d26-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d3d26-129">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d3d26-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d3d26-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3d26-130">Examples</span></span>

<span data-ttu-id="d3d26-131">Nell'esempio seguente viene illustrato come recuperare il byte di stato SW2 della [*risposta APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d3d26-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="d3d26-132">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d26-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d3d26-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3d26-133">Requirements</span></span>



| <span data-ttu-id="d3d26-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d26-134">Requirement</span></span> | <span data-ttu-id="d3d26-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d3d26-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d26-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d26-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d26-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d3d26-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d3d26-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d26-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d26-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3d26-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3d26-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d3d26-140">End of client support</span></span><br/>    | <span data-ttu-id="d3d26-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d3d26-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d3d26-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="d3d26-142">End of server support</span></span><br/>    | <span data-ttu-id="d3d26-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3d26-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d3d26-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3d26-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d26-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3d26-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d3d26-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3d26-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d3d26-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d3d26-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3d26-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3d26-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3d26-150">IID</span><span class="sxs-lookup"><span data-stu-id="d3d26-150">IID</span></span><br/>                      | <span data-ttu-id="d3d26-151">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d3d26-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d3d26-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3d26-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d26-153">**ottenere \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="d3d26-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="d3d26-154">**ottenere \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="d3d26-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="d3d26-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d3d26-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
