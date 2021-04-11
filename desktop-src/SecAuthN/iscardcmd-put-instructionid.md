---
description: Imposta l'identificatore di istruzione specificato nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: ea527ffd-b053-467d-883d-b93d5bbfb071
title: 'ISCardCmd: metodo:p ut_InstructionId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_InstructionId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6194accfb834152cf07a58fbb8036b13d3fdcd5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966923"
---
# <a name="iscardcmdput_instructionid-method"></a><span data-ttu-id="c42d4-103">ISCardCmd::p UT \_ InstructionId metodo</span><span class="sxs-lookup"><span data-stu-id="c42d4-103">ISCardCmd::put\_InstructionId method</span></span>

<span data-ttu-id="c42d4-104">\[Il metodo **put \_ InstructionId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c42d4-104">\[The **put\_InstructionId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c42d4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c42d4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c42d4-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c42d4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c42d4-107">Il metodo **put \_ InstructionId** imposta l'identificatore di istruzione specificato nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="c42d4-107">The **put\_InstructionId** method sets the given instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="c42d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c42d4-108">Syntax</span></span>


```C++
HRESULT put_InstructionId(
  [in] BYTE byIns
);
```



## <a name="parameters"></a><span data-ttu-id="c42d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c42d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c42d4-110">*byIns* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c42d4-110">*byIns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c42d4-111">Byte che rappresenta l'identificatore dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="c42d4-111">The byte that is the instruction identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c42d4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c42d4-112">Return value</span></span>

<span data-ttu-id="c42d4-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="c42d4-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c42d4-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c42d4-114">Return code</span></span>                                                                                   | <span data-ttu-id="c42d4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c42d4-115">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c42d4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c42d4-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c42d4-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="c42d4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c42d4-119">Il parametro *byIns* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c42d4-119">The *byIns* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c42d4-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c42d4-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c42d4-121">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="c42d4-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c42d4-122">Remarks</span></span>

<span data-ttu-id="c42d4-123">Per ottenere l'identificatore di istruzioni esistente, chiamare [**get \_ InstructionId**](iscardcmd-get-instructionid.md).</span><span class="sxs-lookup"><span data-stu-id="c42d4-123">To get the existing instructional identifier, call [**get\_InstructionId**](iscardcmd-get-instructionid.md).</span></span>

<span data-ttu-id="c42d4-124">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c42d4-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c42d4-125">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c42d4-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c42d4-126">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c42d4-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c42d4-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="c42d4-127">Examples</span></span>

<span data-ttu-id="c42d4-128">Nell'esempio seguente viene illustrato come impostare un identificatore di istruzione nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="c42d4-128">The following example shows how to set an instruction identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="c42d4-129">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c42d4-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT hr;

// Set the instruction ID.
hr = pISCardCmd->put_InstructionId(0xb2);
if (FAILED(hr))
{
  printf("Failed put_InstructionId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c42d4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c42d4-130">Requirements</span></span>



| <span data-ttu-id="c42d4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c42d4-131">Requirement</span></span> | <span data-ttu-id="c42d4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c42d4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c42d4-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c42d4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c42d4-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c42d4-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c42d4-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c42d4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c42d4-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c42d4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c42d4-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c42d4-137">End of client support</span></span><br/>    | <span data-ttu-id="c42d4-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c42d4-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c42d4-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c42d4-139">End of server support</span></span><br/>    | <span data-ttu-id="c42d4-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c42d4-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c42d4-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c42d4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c42d4-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c42d4-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c42d4-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c42d4-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c42d4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c42d4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c42d4-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c42d4-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c42d4-147">IID</span><span class="sxs-lookup"><span data-stu-id="c42d4-147">IID</span></span><br/>                      | <span data-ttu-id="c42d4-148">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c42d4-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c42d4-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c42d4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c42d4-150">**ottenere \_ InstructionId**</span><span class="sxs-lookup"><span data-stu-id="c42d4-150">**get\_InstructionId**</span></span>](iscardcmd-get-instructionid.md)
</dt> <dt>

[<span data-ttu-id="c42d4-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="c42d4-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
