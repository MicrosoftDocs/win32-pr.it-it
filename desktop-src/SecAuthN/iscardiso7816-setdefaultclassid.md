---
description: Il metodo SetDefaultClassId assegna un byte dell'identificatore di classe standard che verrà usato in tutte le operazioni quando si costruisce un'unità dati del protocollo ISO 7816-4 (APDU). Per impostazione predefinita, il byte dell'identificatore di classe standard è 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'Metodo ISCardISO7816:: SetDefaultClassId (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313739"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="8480f-104">Metodo ISCardISO7816:: SetDefaultClassId</span><span class="sxs-lookup"><span data-stu-id="8480f-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="8480f-105">\[Il metodo **SetDefaultClassId** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8480f-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8480f-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8480f-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8480f-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8480f-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8480f-108">Il metodo **SetDefaultClassId** assegna un byte dell'identificatore di classe standard che verrà usato in tutte le operazioni quando si costruisce un' [*unità dati del protocollo*](../secgloss/a-gly.md) ISO 7816-4 (APDU).</span><span class="sxs-lookup"><span data-stu-id="8480f-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="8480f-109">Per impostazione predefinita, il byte dell'identificatore di classe standard è 0x00.</span><span class="sxs-lookup"><span data-stu-id="8480f-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="8480f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8480f-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="8480f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8480f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8480f-112">*byClass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8480f-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8480f-113">Byte ID classe.</span><span class="sxs-lookup"><span data-stu-id="8480f-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8480f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8480f-114">Return value</span></span>

<span data-ttu-id="8480f-115">I possibili valori restituiti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8480f-115">The possible return values are the following:</span></span>



| <span data-ttu-id="8480f-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8480f-116">Return code</span></span>                                                                          | <span data-ttu-id="8480f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8480f-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8480f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8480f-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8480f-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8480f-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="8480f-120">Per un elenco di tutti i metodi forniti dall'interfaccia [**ISCardISO7816**](iscardiso7816.md) , vedere **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="8480f-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="8480f-121">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8480f-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8480f-122">Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8480f-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8480f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8480f-123">Requirements</span></span>



| <span data-ttu-id="8480f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8480f-124">Requirement</span></span> | <span data-ttu-id="8480f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8480f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8480f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8480f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8480f-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8480f-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8480f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8480f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8480f-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8480f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8480f-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8480f-130">End of client support</span></span><br/>    | <span data-ttu-id="8480f-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8480f-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8480f-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8480f-132">End of server support</span></span><br/>    | <span data-ttu-id="8480f-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8480f-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8480f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8480f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8480f-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8480f-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8480f-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8480f-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="8480f-137"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8480f-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8480f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8480f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8480f-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8480f-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8480f-140">IID</span><span class="sxs-lookup"><span data-stu-id="8480f-140">IID</span></span><br/>                      | <span data-ttu-id="8480f-141">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8480f-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8480f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8480f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8480f-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8480f-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
