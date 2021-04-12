---
description: Il metodo Clear cancella i buffer dei messaggi APDU (Application Protocol Data Unit) e Reply APDU.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'Metodo ISCardCmd:: Clear (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129354"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="87dd8-103">Metodo ISCardCmd:: Clear</span><span class="sxs-lookup"><span data-stu-id="87dd8-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="87dd8-104">\[Il metodo **Clear** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="87dd8-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87dd8-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87dd8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="87dd8-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="87dd8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="87dd8-107">Il metodo **Clear** Cancella i buffer dei messaggi APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) e [*Reply APDU*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="87dd8-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="87dd8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87dd8-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="87dd8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="87dd8-109">Parameters</span></span>

<span data-ttu-id="87dd8-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="87dd8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87dd8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87dd8-111">Return value</span></span>

<span data-ttu-id="87dd8-112">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="87dd8-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="87dd8-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87dd8-113">Return code</span></span>                                                                             | <span data-ttu-id="87dd8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87dd8-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="87dd8-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87dd8-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="87dd8-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="87dd8-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="87dd8-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="87dd8-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="87dd8-118">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="87dd8-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="87dd8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="87dd8-119">Remarks</span></span>

<span data-ttu-id="87dd8-120">Per compilare un comando APDU, chiamare [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="87dd8-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="87dd8-121">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="87dd8-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="87dd8-122">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="87dd8-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="87dd8-123">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="87dd8-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="87dd8-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="87dd8-124">Examples</span></span>

<span data-ttu-id="87dd8-125">Nell'esempio seguente viene illustrato come cancellare i buffer dei messaggi APDU APDU e Reply.</span><span class="sxs-lookup"><span data-stu-id="87dd8-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="87dd8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87dd8-126">Requirements</span></span>



| <span data-ttu-id="87dd8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87dd8-127">Requirement</span></span> | <span data-ttu-id="87dd8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="87dd8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87dd8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87dd8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="87dd8-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87dd8-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="87dd8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87dd8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="87dd8-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87dd8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87dd8-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="87dd8-133">End of client support</span></span><br/>    | <span data-ttu-id="87dd8-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="87dd8-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="87dd8-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="87dd8-135">End of server support</span></span><br/>    | <span data-ttu-id="87dd8-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87dd8-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="87dd8-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87dd8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="87dd8-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="87dd8-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="87dd8-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="87dd8-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="87dd8-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="87dd8-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="87dd8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="87dd8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87dd8-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87dd8-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="87dd8-143">IID</span><span class="sxs-lookup"><span data-stu-id="87dd8-143">IID</span></span><br/>                      | <span data-ttu-id="87dd8-144">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="87dd8-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="87dd8-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87dd8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87dd8-146">**ISCardCmd::BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="87dd8-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="87dd8-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="87dd8-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
