---
description: Recupera il terzo parametro (P3) byte dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'Metodo ISCardCmd:: get_P3 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129339"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="7c45e-103">Metodo ISCardCmd:: Get \_ P3</span><span class="sxs-lookup"><span data-stu-id="7c45e-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="7c45e-104">\[Il metodo **get \_ P3** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7c45e-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7c45e-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7c45e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c45e-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7c45e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7c45e-107">Il metodo **get \_ P3** Recupera il terzo parametro (P3) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="7c45e-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7c45e-108">Questo valore di byte di sola lettura rappresenta le dimensioni della parte di dati di APDU.</span><span class="sxs-lookup"><span data-stu-id="7c45e-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c45e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c45e-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="7c45e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c45e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c45e-111">*pbyP3* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7c45e-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45e-112">Puntatore al byte che rappresenta il P3 da APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="7c45e-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c45e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c45e-113">Return value</span></span>

<span data-ttu-id="7c45e-114">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="7c45e-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7c45e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7c45e-115">Return code</span></span>                                                                                   | <span data-ttu-id="7c45e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c45e-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7c45e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7c45e-118">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="7c45e-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="7c45e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7c45e-120">*PbyP3* non valido.</span><span class="sxs-lookup"><span data-stu-id="7c45e-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="7c45e-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7c45e-122">Un puntatore errato è stato passato in *pbyP3*.</span><span class="sxs-lookup"><span data-stu-id="7c45e-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="7c45e-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7c45e-124">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7c45e-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="7c45e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c45e-125">Remarks</span></span>

<span data-ttu-id="7c45e-126">Il parametro P3 è di sola lettura e pertanto non può essere impostato.</span><span class="sxs-lookup"><span data-stu-id="7c45e-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="7c45e-127">Per ottenere i parametri P1 o P2, chiamare rispettivamente [**get \_ P1**](iscardcmd-get-p1.md) e [**get \_ P2**](iscardcmd-get-p2.md) .</span><span class="sxs-lookup"><span data-stu-id="7c45e-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="7c45e-128">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="7c45e-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="7c45e-129">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="7c45e-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7c45e-130">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7c45e-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7c45e-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="7c45e-131">Examples</span></span>

<span data-ttu-id="7c45e-132">Nell'esempio seguente viene illustrato come recuperare il terzo parametro (P3) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="7c45e-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="7c45e-133">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="7c45e-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="7c45e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c45e-134">Requirements</span></span>



| <span data-ttu-id="7c45e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c45e-135">Requirement</span></span> | <span data-ttu-id="7c45e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="7c45e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c45e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c45e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7c45e-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7c45e-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c45e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c45e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7c45e-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c45e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c45e-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7c45e-141">End of client support</span></span><br/>    | <span data-ttu-id="7c45e-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c45e-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7c45e-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7c45e-143">End of server support</span></span><br/>    | <span data-ttu-id="7c45e-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c45e-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7c45e-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c45e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c45e-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c45e-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7c45e-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c45e-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c45e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7c45e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c45e-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c45e-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c45e-151">IID</span><span class="sxs-lookup"><span data-stu-id="7c45e-151">IID</span></span><br/>                      | <span data-ttu-id="7c45e-152">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7c45e-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7c45e-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c45e-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c45e-154">**ottenere \_ P1**</span><span class="sxs-lookup"><span data-stu-id="7c45e-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="7c45e-155">**ottenere \_ P2**</span><span class="sxs-lookup"><span data-stu-id="7c45e-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="7c45e-156">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="7c45e-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
