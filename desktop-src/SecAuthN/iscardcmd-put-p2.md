---
description: Imposta il secondo parametro (P2) byte nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 8d11b967-33cd-4bfa-b294-cc0c422cf6cf
title: 'ISCardCmd: metodo:p ut_P2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 362da530dece37a0a0ca600b1edb414d29e1bd48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225901"
---
# <a name="iscardcmdput_p2-method"></a><span data-ttu-id="4d3fb-103">ISCardCmd::p il \_ Metodo UT P2</span><span class="sxs-lookup"><span data-stu-id="4d3fb-103">ISCardCmd::put\_P2 method</span></span>

<span data-ttu-id="4d3fb-104">\[Il metodo **put \_ p2** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-104">\[The **put\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4d3fb-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d3fb-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4d3fb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4d3fb-107">Il metodo **put \_ p2** imposta il secondo parametro (P2) byte nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4d3fb-107">The **put\_P2** method sets the second parameter (P2) byte in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3fb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d3fb-108">Syntax</span></span>


```C++
HRESULT put_P2(
  [in] BYTE byP2
);
```



## <a name="parameters"></a><span data-ttu-id="4d3fb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d3fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d3fb-110">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d3fb-110">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3fb-111">Byte che rappresenta il campo P2.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-111">The byte that is the P2 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d3fb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d3fb-112">Return value</span></span>

<span data-ttu-id="4d3fb-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4d3fb-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4d3fb-114">Return code</span></span>                                                                                   | <span data-ttu-id="4d3fb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d3fb-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="4d3fb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4d3fb-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="4d3fb-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4d3fb-119">Il parametro *byP2* non è valido.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-119">The *byP2* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4d3fb-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4d3fb-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4d3fb-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d3fb-122">Remarks</span></span>

<span data-ttu-id="4d3fb-123">Per impostare il valore P1 di APDU, chiamare [**put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="4d3fb-123">To set the P1 value of the APDU, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="4d3fb-124">Per recuperare i valori P1, P2 e P3 esistenti, chiamare [**get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) o [**get \_ P3**](iscardcmd-get-p3.md) rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="4d3fb-125">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4d3fb-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4d3fb-126">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4d3fb-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4d3fb-127">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4d3fb-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4d3fb-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="4d3fb-128">Examples</span></span>

<span data-ttu-id="4d3fb-129">Nell'esempio seguente viene illustrato come impostare il secondo parametro (P2) byte dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4d3fb-129">The following example shows how to set the second parameter (P2) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="4d3fb-130">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4d3fb-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P2 byte.
hr = pISCardCmd->put_P2(0x06);
if (FAILED(hr))
{
  printf("Failed put_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4d3fb-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d3fb-131">Requirements</span></span>



| <span data-ttu-id="4d3fb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d3fb-132">Requirement</span></span> | <span data-ttu-id="4d3fb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4d3fb-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3fb-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d3fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3fb-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d3fb-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4d3fb-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d3fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3fb-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d3fb-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d3fb-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4d3fb-138">End of client support</span></span><br/>    | <span data-ttu-id="4d3fb-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d3fb-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4d3fb-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4d3fb-140">End of server support</span></span><br/>    | <span data-ttu-id="4d3fb-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d3fb-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4d3fb-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d3fb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d3fb-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d3fb-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4d3fb-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d3fb-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d3fb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4d3fb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d3fb-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d3fb-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d3fb-148">IID</span><span class="sxs-lookup"><span data-stu-id="4d3fb-148">IID</span></span><br/>                      | <span data-ttu-id="4d3fb-149">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4d3fb-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4d3fb-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d3fb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d3fb-151">**ottenere \_ P1**</span><span class="sxs-lookup"><span data-stu-id="4d3fb-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="4d3fb-152">**ottenere \_ P2**</span><span class="sxs-lookup"><span data-stu-id="4d3fb-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="4d3fb-153">**ottenere \_ P3**</span><span class="sxs-lookup"><span data-stu-id="4d3fb-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="4d3fb-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4d3fb-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4d3fb-155">**Inserisci \_ P1**</span><span class="sxs-lookup"><span data-stu-id="4d3fb-155">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
