---
description: Imposta il primo parametro (P1) byte dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'ISCardCmd: metodo:p ut_P1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314738"
---
# <a name="iscardcmdput_p1-method"></a><span data-ttu-id="9d59c-103">ISCardCmd::p UT \_ P1 (metodo)</span><span class="sxs-lookup"><span data-stu-id="9d59c-103">ISCardCmd::put\_P1 method</span></span>

<span data-ttu-id="9d59c-104">\[Il metodo **put \_ P1** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9d59c-104">\[The **put\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d59c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9d59c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9d59c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="9d59c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9d59c-107">Il metodo **put \_ P1** imposta il primo parametro (P1) byte dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="9d59c-107">The **put\_P1** method sets the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d59c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d59c-108">Syntax</span></span>


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a><span data-ttu-id="9d59c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d59c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d59c-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d59c-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d59c-111">Byte che rappresenta il campo P1.</span><span class="sxs-lookup"><span data-stu-id="9d59c-111">The byte that is the P1 field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d59c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d59c-112">Return value</span></span>

<span data-ttu-id="9d59c-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="9d59c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9d59c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9d59c-114">Return code</span></span>                                                                                   | <span data-ttu-id="9d59c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d59c-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9d59c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9d59c-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="9d59c-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="9d59c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9d59c-119">Il parametro *byP1* non è valido.</span><span class="sxs-lookup"><span data-stu-id="9d59c-119">The *byP1* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="9d59c-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9d59c-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9d59c-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9d59c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d59c-122">Remarks</span></span>

<span data-ttu-id="9d59c-123">Per impostare il valore P2 di APDU, chiamare [**get \_ p2**](iscardcmd-get-p2.md).</span><span class="sxs-lookup"><span data-stu-id="9d59c-123">To set the P2 value of the APDU, call [**get\_P2**](iscardcmd-get-p2.md).</span></span>

<span data-ttu-id="9d59c-124">Per recuperare i valori P1, P2 e P3 esistenti, chiamare [**get \_ P1**](iscardcmd-get-p1.md), [**get \_ P2**](iscardcmd-get-p2.md) o [**get \_ P3**](iscardcmd-get-p3.md) rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="9d59c-124">To retrieve the existing P1, P2, and P3 values, call [**get\_P1**](iscardcmd-get-p1.md), [**get\_P2**](iscardcmd-get-p2.md) or [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="9d59c-125">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="9d59c-125">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="9d59c-126">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="9d59c-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9d59c-127">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9d59c-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9d59c-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="9d59c-128">Examples</span></span>

<span data-ttu-id="9d59c-129">Nell'esempio seguente viene illustrato come impostare il primo parametro (P1) byte dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="9d59c-129">The following example shows how to set the first parameter (P1) byte of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="9d59c-130">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="9d59c-130">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9d59c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d59c-131">Requirements</span></span>



| <span data-ttu-id="9d59c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d59c-132">Requirement</span></span> | <span data-ttu-id="9d59c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9d59c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d59c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d59c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9d59c-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d59c-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9d59c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d59c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9d59c-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d59c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d59c-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9d59c-138">End of client support</span></span><br/>    | <span data-ttu-id="9d59c-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d59c-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9d59c-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9d59c-140">End of server support</span></span><br/>    | <span data-ttu-id="9d59c-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d59c-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9d59c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9d59c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d59c-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d59c-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9d59c-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d59c-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d59c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9d59c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d59c-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d59c-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d59c-148">IID</span><span class="sxs-lookup"><span data-stu-id="9d59c-148">IID</span></span><br/>                      | <span data-ttu-id="9d59c-149">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9d59c-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9d59c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d59c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d59c-151">**ottenere \_ P1**</span><span class="sxs-lookup"><span data-stu-id="9d59c-151">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="9d59c-152">**ottenere \_ P2**</span><span class="sxs-lookup"><span data-stu-id="9d59c-152">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="9d59c-153">**ottenere \_ P3**</span><span class="sxs-lookup"><span data-stu-id="9d59c-153">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="9d59c-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="9d59c-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="9d59c-155">**Inserisci \_ P2**</span><span class="sxs-lookup"><span data-stu-id="9d59c-155">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
