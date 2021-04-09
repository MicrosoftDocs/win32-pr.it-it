---
description: Recupera il secondo parametro (P2) byte dall'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: c719786f-0f50-472e-a92e-a64c333fc255
title: 'Metodo ISCardCmd:: get_P2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7811ad3e42264477210830f340338d0786ed5547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129338"
---
# <a name="iscardcmdget_p2-method"></a><span data-ttu-id="a16a6-103">Metodo ISCardCmd:: Get \_ P2</span><span class="sxs-lookup"><span data-stu-id="a16a6-103">ISCardCmd::get\_P2 method</span></span>

<span data-ttu-id="a16a6-104">\[Il metodo **get \_ p2** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a16a6-104">\[The **get\_P2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a16a6-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a16a6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a16a6-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a16a6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a16a6-107">Il metodo **get \_ p2** Recupera il secondo parametro (P2) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a16a6-107">The **get\_P2** method retrieves the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="a16a6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a16a6-108">Syntax</span></span>


```C++
HRESULT get_P2(
  [out] BYTE *pbyP2
);
```



## <a name="parameters"></a><span data-ttu-id="a16a6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a16a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16a6-110">*pbyP2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a16a6-110">*pbyP2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a16a6-111">Puntatore al byte che rappresenta il P2 da APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="a16a6-111">Pointer to the byte that is the P2 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16a6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a16a6-112">Return value</span></span>

<span data-ttu-id="a16a6-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a16a6-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a16a6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a16a6-114">Return code</span></span>                                                                                   | <span data-ttu-id="a16a6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a16a6-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a16a6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a16a6-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a16a6-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="a16a6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a16a6-119">Il parametro *pbyP2* non è valido.</span><span class="sxs-lookup"><span data-stu-id="a16a6-119">The *pbyP2* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a16a6-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a16a6-121">Un puntatore errato è stato passato in *pbyP2*.</span><span class="sxs-lookup"><span data-stu-id="a16a6-121">A bad pointer was passed in *pbyP2*.</span></span><br/> |
| <dl> <span data-ttu-id="a16a6-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a16a6-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a16a6-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="a16a6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="a16a6-124">Remarks</span></span>

<span data-ttu-id="a16a6-125">Per impostare il parametro P2 su un nuovo valore, chiamare [**put \_ p2**](iscardcmd-put-p2.md).</span><span class="sxs-lookup"><span data-stu-id="a16a6-125">To set the P2 parameter to a new value, call [**put\_P2**](iscardcmd-put-p2.md).</span></span>

<span data-ttu-id="a16a6-126">Per ottenere i parametri P1 o P3, chiamare rispettivamente [**get \_ P1**](iscardcmd-get-p1.md) e [**get \_ P3**](iscardcmd-get-p3.md) .</span><span class="sxs-lookup"><span data-stu-id="a16a6-126">To get the P1 or P3 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P3**](iscardcmd-get-p3.md) respectively.</span></span>

<span data-ttu-id="a16a6-127">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="a16a6-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="a16a6-128">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a16a6-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a16a6-129">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a16a6-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a16a6-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="a16a6-130">Examples</span></span>

<span data-ttu-id="a16a6-131">Nell'esempio seguente viene illustrato come recuperare il secondo parametro (P2) byte dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="a16a6-131">The following example shows how to retrieve the second parameter (P2) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="a16a6-132">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="a16a6-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP2;
HRESULT  hr;

// Retrieve the P2 byte.
hr = pISCardCmd->get_P2(&byP2);
if (FAILED(hr))
{
  printf("Failed get_P2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="a16a6-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a16a6-133">Requirements</span></span>



| <span data-ttu-id="a16a6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16a6-134">Requirement</span></span> | <span data-ttu-id="a16a6-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a16a6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16a6-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a16a6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a16a6-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a16a6-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a16a6-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a16a6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a16a6-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a16a6-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a16a6-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a16a6-140">End of client support</span></span><br/>    | <span data-ttu-id="a16a6-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a16a6-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a16a6-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a16a6-142">End of server support</span></span><br/>    | <span data-ttu-id="a16a6-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a16a6-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a16a6-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a16a6-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a16a6-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a16a6-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a16a6-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="a16a6-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a16a6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a16a6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16a6-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16a6-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a16a6-150">IID</span><span class="sxs-lookup"><span data-stu-id="a16a6-150">IID</span></span><br/>                      | <span data-ttu-id="a16a6-151">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a16a6-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="a16a6-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a16a6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16a6-153">**ottenere \_ P1**</span><span class="sxs-lookup"><span data-stu-id="a16a6-153">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="a16a6-154">**ottenere \_ P3**</span><span class="sxs-lookup"><span data-stu-id="a16a6-154">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="a16a6-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a16a6-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="a16a6-156">**Inserisci \_ P2**</span><span class="sxs-lookup"><span data-stu-id="a16a6-156">**put\_P2**</span></span>](iscardcmd-put-p2.md)
</dt> </dl>

 

 
