---
description: Costruisce un APDU (Command Application Protocol Data Unit) valido per la trasmissione a una smart card.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'Metodo ISCardCmd:: BuildCmd (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232672"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="58bb1-103">Metodo ISCardCmd:: BuildCmd</span><span class="sxs-lookup"><span data-stu-id="58bb1-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="58bb1-104">\[Il metodo **BuildCmd** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="58bb1-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58bb1-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="58bb1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="58bb1-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="58bb1-107">Il metodo **BuildCmd** crea un' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) del comando (APDU) valida per la trasmissione a una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="58bb1-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="58bb1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58bb1-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="58bb1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="58bb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58bb1-110">*byClassId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-111">Identificatore della classe di comando.</span><span class="sxs-lookup"><span data-stu-id="58bb1-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="58bb1-112">*byInsId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-113">Identificatore dell'istruzione del comando.</span><span class="sxs-lookup"><span data-stu-id="58bb1-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="58bb1-114">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-115">Primo parametro del comando.</span><span class="sxs-lookup"><span data-stu-id="58bb1-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="58bb1-116">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-117">Secondo parametro del comando.</span><span class="sxs-lookup"><span data-stu-id="58bb1-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="58bb1-118">*pbyData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-119">Puntatore alla parte di dati del comando.</span><span class="sxs-lookup"><span data-stu-id="58bb1-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="58bb1-120">*p1Le* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58bb1-121">Puntatore a un valore LONG integer contenente la lunghezza prevista dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="58bb1-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58bb1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58bb1-122">Return value</span></span>

<span data-ttu-id="58bb1-123">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="58bb1-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="58bb1-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="58bb1-124">Return code</span></span>                                                                                   | <span data-ttu-id="58bb1-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58bb1-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="58bb1-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="58bb1-127">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="58bb1-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="58bb1-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="58bb1-129">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="58bb1-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="58bb1-130"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="58bb1-131">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="58bb1-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="58bb1-132"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="58bb1-133">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="58bb1-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="58bb1-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="58bb1-134">Remarks</span></span>

<span data-ttu-id="58bb1-135">Per incapsulare il comando in un altro comando, chiamare [**incapsulate**](iscardcmd-encapsulate.md).</span><span class="sxs-lookup"><span data-stu-id="58bb1-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="58bb1-136">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="58bb1-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="58bb1-137">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="58bb1-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="58bb1-138">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="58bb1-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="58bb1-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="58bb1-139">Examples</span></span>

<span data-ttu-id="58bb1-140">Nell'esempio seguente viene illustrato come creare un comando APDU.</span><span class="sxs-lookup"><span data-stu-id="58bb1-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="58bb1-141">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) e che pIByteRequest sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) inizializzata con una chiamata precedente al metodo [**IByteBuffer:: Initialize**](ibytebuffer-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="58bb1-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="58bb1-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58bb1-142">Requirements</span></span>



| <span data-ttu-id="58bb1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="58bb1-143">Requirement</span></span> | <span data-ttu-id="58bb1-144">Valore</span><span class="sxs-lookup"><span data-stu-id="58bb1-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58bb1-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58bb1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="58bb1-146">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="58bb1-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58bb1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="58bb1-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58bb1-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58bb1-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="58bb1-149">End of client support</span></span><br/>    | <span data-ttu-id="58bb1-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="58bb1-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="58bb1-151">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="58bb1-151">End of server support</span></span><br/>    | <span data-ttu-id="58bb1-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58bb1-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="58bb1-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58bb1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="58bb1-154"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="58bb1-155">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="58bb1-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="58bb1-156"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58bb1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="58bb1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58bb1-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58bb1-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="58bb1-159">IID</span><span class="sxs-lookup"><span data-stu-id="58bb1-159">IID</span></span><br/>                      | <span data-ttu-id="58bb1-160">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="58bb1-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="58bb1-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58bb1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bb1-162">**Incapsulare**</span><span class="sxs-lookup"><span data-stu-id="58bb1-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="58bb1-163">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="58bb1-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
