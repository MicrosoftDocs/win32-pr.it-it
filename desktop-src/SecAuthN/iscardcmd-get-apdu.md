---
description: Recupera l'unità dati del protocollo applicazione non elaborata (APDU).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Metodo ISCardCmd:: get_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049506"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="ad228-103">Metodo ISCardCmd:: Get \_ APDU</span><span class="sxs-lookup"><span data-stu-id="ad228-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="ad228-104">\[Il metodo **get \_ APDU** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ad228-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ad228-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad228-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ad228-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ad228-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ad228-107">Il metodo **get \_ APDU** recupera l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) non elaborata (APDU).</span><span class="sxs-lookup"><span data-stu-id="ad228-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad228-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad228-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="ad228-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad228-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad228-110">*ppApdu* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ad228-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad228-111">Puntatore al buffer di byte mappato tramite un oggetto **IStream** che contiene il messaggio APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="ad228-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad228-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad228-112">Return value</span></span>

<span data-ttu-id="ad228-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad228-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ad228-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ad228-114">Return code</span></span>                                                                                   | <span data-ttu-id="ad228-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad228-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ad228-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ad228-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ad228-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ad228-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ad228-119">Il parametro *ppApdu* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ad228-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ad228-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ad228-121">Un puntatore errato è stato passato in *ppApdu*.</span><span class="sxs-lookup"><span data-stu-id="ad228-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="ad228-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ad228-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ad228-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ad228-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad228-124">Remarks</span></span>

<span data-ttu-id="ad228-125">Per copiare APDU da un oggetto [**IByteBuffer**](ibytebuffer.md) (**IStream**) in APDU di cui è stato eseguito il wrapper in questo oggetto interfaccia, chiamare [**put \_ APDU**](iscardcmd-put-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="ad228-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="ad228-126">Per determinare la lunghezza di APDU, chiamare [**get \_ ApduLength**](iscardcmd-get-apdulength.md).</span><span class="sxs-lookup"><span data-stu-id="ad228-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="ad228-127">Per un elenco di tutti i metodi forniti dall'interfaccia [**ISCardCmd**](iscardcmd.md) , vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ad228-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ad228-128">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ad228-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ad228-129">Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ad228-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ad228-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad228-130">Examples</span></span>

<span data-ttu-id="ad228-131">Nell'esempio seguente viene illustrato come recuperare l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) non elaborata (APDU).</span><span class="sxs-lookup"><span data-stu-id="ad228-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="ad228-132">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido all'interfaccia [**ISCardCmd**](iscardcmd.md) e che pIByteApdu sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ad228-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ad228-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad228-133">Requirements</span></span>



| <span data-ttu-id="ad228-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad228-134">Requirement</span></span> | <span data-ttu-id="ad228-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ad228-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad228-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad228-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ad228-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad228-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ad228-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad228-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ad228-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad228-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad228-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ad228-140">End of client support</span></span><br/>    | <span data-ttu-id="ad228-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ad228-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ad228-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ad228-142">End of server support</span></span><br/>    | <span data-ttu-id="ad228-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad228-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ad228-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad228-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad228-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad228-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ad228-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad228-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ad228-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ad228-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad228-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad228-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad228-150">IID</span><span class="sxs-lookup"><span data-stu-id="ad228-150">IID</span></span><br/>                      | <span data-ttu-id="ad228-151">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ad228-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ad228-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad228-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad228-153">**ottenere \_ ApduLength**</span><span class="sxs-lookup"><span data-stu-id="ad228-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="ad228-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ad228-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="ad228-155">**Inserisci \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="ad228-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
