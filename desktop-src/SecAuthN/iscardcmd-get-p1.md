---
description: Recupera il primo parametro (P1) byte dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'Metodo ISCardCmd:: get_P1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 047732fd8602828cc0501d623c57653bfdc9044f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526353"
---
# <a name="iscardcmdget_p1-method"></a><span data-ttu-id="4c05e-103">Metodo ISCardCmd:: Get \_ P1</span><span class="sxs-lookup"><span data-stu-id="4c05e-103">ISCardCmd::get\_P1 method</span></span>

<span data-ttu-id="4c05e-104">\[Il metodo **get \_ P1** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="4c05e-104">\[The **get\_P1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c05e-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4c05e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c05e-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4c05e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4c05e-107">Il metodo **get \_ P1** Recupera il primo parametro (P1) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4c05e-107">The **get\_P1** method retrieves the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c05e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c05e-108">Syntax</span></span>


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a><span data-ttu-id="4c05e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c05e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c05e-110">*pbyP1* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c05e-110">*pbyP1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c05e-111">Puntatore al byte P1 in APDU alla restituzione.</span><span class="sxs-lookup"><span data-stu-id="4c05e-111">Pointer to the P1 byte in the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c05e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c05e-112">Return value</span></span>

<span data-ttu-id="4c05e-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="4c05e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4c05e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4c05e-114">Return code</span></span>                                                                                   | <span data-ttu-id="4c05e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c05e-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="4c05e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c05e-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="4c05e-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="4c05e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4c05e-119">Il parametro *pbyP1* non è valido.</span><span class="sxs-lookup"><span data-stu-id="4c05e-119">The *pbyP1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4c05e-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4c05e-121">Un puntatore errato è stato passato in *pbyP1*.</span><span class="sxs-lookup"><span data-stu-id="4c05e-121">A bad pointer was passed in *pbyP1*.</span></span><br/> |
| <dl> <span data-ttu-id="4c05e-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c05e-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4c05e-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="4c05e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c05e-124">Remarks</span></span>

<span data-ttu-id="4c05e-125">Per impostare il parametro P1 su un nuovo valore, chiamare [**put \_ P1**](iscardcmd-put-p1.md).</span><span class="sxs-lookup"><span data-stu-id="4c05e-125">To set the P1 parameter to a new value, call [**put\_P1**](iscardcmd-put-p1.md).</span></span>

<span data-ttu-id="4c05e-126">Per ottenere i parametri P2 o P3, chiamare [**get \_ p2**](iscardcmd-get-p2.md) e [**ottenere rispettivamente \_ P3**](iscardcmd-get-p3.md) .</span><span class="sxs-lookup"><span data-stu-id="4c05e-126">To get the P2 or P3 parameters, call [**get\_P2**](iscardcmd-get-p2.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="4c05e-127">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4c05e-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4c05e-128">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c05e-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4c05e-129">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4c05e-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4c05e-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="4c05e-130">Examples</span></span>

<span data-ttu-id="4c05e-131">Nell'esempio seguente viene illustrato come recuperare il primo parametro (P1) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4c05e-131">The following example shows how to retrieve the first parameter (P1) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="4c05e-132">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4c05e-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4c05e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c05e-133">Requirements</span></span>



| <span data-ttu-id="4c05e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c05e-134">Requirement</span></span> | <span data-ttu-id="4c05e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4c05e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c05e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c05e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4c05e-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c05e-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4c05e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c05e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4c05e-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c05e-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c05e-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4c05e-140">End of client support</span></span><br/>    | <span data-ttu-id="4c05e-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c05e-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4c05e-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4c05e-142">End of server support</span></span><br/>    | <span data-ttu-id="4c05e-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c05e-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4c05e-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c05e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c05e-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c05e-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4c05e-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c05e-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c05e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4c05e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c05e-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c05e-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c05e-150">IID</span><span class="sxs-lookup"><span data-stu-id="4c05e-150">IID</span></span><br/>                      | <span data-ttu-id="4c05e-151">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4c05e-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4c05e-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c05e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c05e-153">**ottenere \_ P2**</span><span class="sxs-lookup"><span data-stu-id="4c05e-153">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="4c05e-154">**ottenere \_ P3**</span><span class="sxs-lookup"><span data-stu-id="4c05e-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="4c05e-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4c05e-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4c05e-156">**Inserisci \_ P1**</span><span class="sxs-lookup"><span data-stu-id="4c05e-156">**put\_P1**</span></span>](iscardcmd-put-p1.md)
</dt> </dl>

 

 
