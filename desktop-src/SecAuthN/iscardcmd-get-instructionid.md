---
description: Recupera il byte dell'identificatore di istruzione dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 294f51cd-0a13-4dfb-bf02-9edd11a7085e
title: 'Metodo ISCardCmd:: get_InstructionId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4b0125237ef94a5d6173f517483b9ae8781d5607
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968573"
---
# <a name="iscardcmdget_instructionid-method"></a><span data-ttu-id="a349f-103">Metodo ISCardCmd:: Get \_ InstructionId</span><span class="sxs-lookup"><span data-stu-id="a349f-103">ISCardCmd::get\_InstructionId method</span></span>

<span data-ttu-id="a349f-104">\[Il metodo **get \_ InstructionId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a349f-104">\[The **get\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a349f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a349f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a349f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a349f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a349f-107">Il metodo **get \_ InstructionId** Recupera il byte dell'identificatore di istruzione dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a349f-107">The **get\_InstructionId** method retrieves the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a349f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a349f-108">Syntax</span></span>


```C++
HRESULT get_InstructionId(
  [out] BYTE *pbyIns
);
```



## <a name="parameters"></a><span data-ttu-id="a349f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a349f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a349f-110">*pbyIns* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a349f-110">*pbyIns* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a349f-111">Puntatore al byte che rappresenta l'ID di istruzione da APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="a349f-111">Pointer to the byte that is the instruction ID from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a349f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a349f-112">Return value</span></span>

<span data-ttu-id="a349f-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a349f-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a349f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a349f-114">Return code</span></span>                                                                                   | <span data-ttu-id="a349f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a349f-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="a349f-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a349f-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a349f-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a349f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a349f-119">Il parametro *pbyIns* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a349f-119">The *pbyIns* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a349f-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a349f-121">Un puntatore errato è stato passato in *pbyIns*.</span><span class="sxs-lookup"><span data-stu-id="a349f-121">A bad pointer was passed in *pbyIns*.</span></span><br/> |
| <dl> <span data-ttu-id="a349f-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a349f-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a349f-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a349f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="a349f-124">Remarks</span></span>

<span data-ttu-id="a349f-125">Per impostare l'identificatore dell'istruzione su un nuovo valore, chiamare [**put \_ InstructionId**](iscardcmd-put-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="a349f-125">To set the instructional identifier to a new value, call [**put\_InstructionId**](iscardcmd-put-instructionid.md).</span></span>

<span data-ttu-id="a349f-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a349f-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a349f-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a349f-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a349f-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a349f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a349f-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="a349f-129">Examples</span></span>

<span data-ttu-id="a349f-130">Nell'esempio seguente viene illustrato come recuperare il byte dell'identificatore di istruzione dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a349f-130">The following example shows how to retrieve the instruction identifier byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a349f-131">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a349f-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byInstructID;
HRESULT hr;

// Retrieve the instruction ID.
hr = pISCardCmd->get_InstructionId(&byInstructID);
if (FAILED(hr))
{
  printf("Failed get_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a349f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a349f-132">Requirements</span></span>



| <span data-ttu-id="a349f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a349f-133">Requirement</span></span> | <span data-ttu-id="a349f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a349f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a349f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a349f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a349f-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a349f-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a349f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a349f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a349f-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a349f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a349f-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a349f-139">End of client support</span></span><br/>    | <span data-ttu-id="a349f-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a349f-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a349f-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a349f-141">End of server support</span></span><br/>    | <span data-ttu-id="a349f-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a349f-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a349f-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a349f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a349f-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a349f-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a349f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="a349f-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a349f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a349f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a349f-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a349f-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a349f-149">IID</span><span class="sxs-lookup"><span data-stu-id="a349f-149">IID</span></span><br/>                      | <span data-ttu-id="a349f-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a349f-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a349f-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a349f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a349f-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a349f-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a349f-153">**Inserisci \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="a349f-153">**put\_InstructionId**</span></span>](iscardcmd-put-instructionid.md)
</dt> </dl>

 

 
