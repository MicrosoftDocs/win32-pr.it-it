---
description: Imposta un nuovo identificatore di classe nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'ISCardCmd: metodo:p ut_ClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966924"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="bfa0c-103">ISCardCmd: metodo:p UT \_ ClassID</span><span class="sxs-lookup"><span data-stu-id="bfa0c-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="bfa0c-104">\[Il metodo **put \_ ClassID** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bfa0c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bfa0c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bfa0c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bfa0c-107">Il metodo **put \_ ClassID** imposta un nuovo identificatore di classe nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="bfa0c-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa0c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfa0c-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="bfa0c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfa0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa0c-110">*byClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfa0c-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa0c-111">Byte che rappresenta l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa0c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfa0c-112">Return value</span></span>

<span data-ttu-id="bfa0c-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bfa0c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bfa0c-114">Return code</span></span>                                                                                   | <span data-ttu-id="bfa0c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa0c-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bfa0c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bfa0c-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bfa0c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bfa0c-119">*ByClass* non valido.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="bfa0c-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bfa0c-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bfa0c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfa0c-122">Remarks</span></span>

<span data-ttu-id="bfa0c-123">Per recuperare l'identificatore di classe corrente, chiamare [**get \_ ClassID**](iscardcmd-get-classid.md).</span><span class="sxs-lookup"><span data-stu-id="bfa0c-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="bfa0c-124">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bfa0c-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="bfa0c-125">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bfa0c-126">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bfa0c-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bfa0c-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="bfa0c-127">Examples</span></span>

<span data-ttu-id="bfa0c-128">Nell'esempio seguente viene illustrato come impostare un nuovo identificatore di classe nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="bfa0c-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="bfa0c-129">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa0c-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="bfa0c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfa0c-130">Requirements</span></span>



| <span data-ttu-id="bfa0c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa0c-131">Requirement</span></span> | <span data-ttu-id="bfa0c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bfa0c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa0c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa0c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa0c-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfa0c-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bfa0c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfa0c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa0c-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfa0c-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bfa0c-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bfa0c-137">End of client support</span></span><br/>    | <span data-ttu-id="bfa0c-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfa0c-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bfa0c-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bfa0c-139">End of server support</span></span><br/>    | <span data-ttu-id="bfa0c-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfa0c-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bfa0c-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfa0c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa0c-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfa0c-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bfa0c-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfa0c-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfa0c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa0c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa0c-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfa0c-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfa0c-147">IID</span><span class="sxs-lookup"><span data-stu-id="bfa0c-147">IID</span></span><br/>                      | <span data-ttu-id="bfa0c-148">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bfa0c-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bfa0c-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfa0c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa0c-150">**ottenere \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="bfa0c-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="bfa0c-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="bfa0c-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
