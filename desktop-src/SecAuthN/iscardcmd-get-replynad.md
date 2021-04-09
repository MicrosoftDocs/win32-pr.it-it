---
description: Recupera l'indirizzo del nodo (NAD) utilizzato dalla smart card nel messaggio di risposta.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Metodo ISCardCmd:: get_ReplyNad (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129335"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="e783f-103">Metodo ISCardCmd:: Get \_ ReplyNad</span><span class="sxs-lookup"><span data-stu-id="e783f-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="e783f-104">\[Il metodo **get \_ ReplyNad** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e783f-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e783f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e783f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e783f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e783f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e783f-107">Il metodo **get \_ ReplyNad** recupera l'indirizzo del nodo (NAD) usato dalla [*Smart Card*](../secgloss/s-gly.md) nel messaggio di risposta.</span><span class="sxs-lookup"><span data-stu-id="e783f-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e783f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e783f-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="e783f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e783f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e783f-110">*pbNad* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e783f-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e783f-111">Puntatore al byte che contiene il nad utilizzato dal messaggio di risposta, al ritorno.</span><span class="sxs-lookup"><span data-stu-id="e783f-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e783f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e783f-112">Return value</span></span>

<span data-ttu-id="e783f-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="e783f-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e783f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e783f-114">Return code</span></span>                                                                                    | <span data-ttu-id="e783f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e783f-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e783f-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="e783f-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e783f-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="e783f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="e783f-119">Il parametro *pbNad* non è valido.</span><span class="sxs-lookup"><span data-stu-id="e783f-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="e783f-120"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="e783f-121">Le chiamate interne non sono in grado di recuperare le informazioni sul NAD.</span><span class="sxs-lookup"><span data-stu-id="e783f-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e783f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e783f-122">Remarks</span></span>

<span data-ttu-id="e783f-123">Oltre ai codici di errore COM elencati in precedenza, questo metodo può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e783f-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e783f-124">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e783f-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e783f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="e783f-125">Examples</span></span>

<span data-ttu-id="e783f-126">Nell'esempio seguente viene illustrato come recuperare l'indirizzo del nodo (NAD) utilizzato dalla [*Smart Card*](../secgloss/s-gly.md) nel messaggio di risposta.</span><span class="sxs-lookup"><span data-stu-id="e783f-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="e783f-127">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="e783f-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e783f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e783f-128">Requirements</span></span>



| <span data-ttu-id="e783f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e783f-129">Requirement</span></span> | <span data-ttu-id="e783f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e783f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e783f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e783f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e783f-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e783f-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e783f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e783f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e783f-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e783f-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e783f-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e783f-135">End of client support</span></span><br/>    | <span data-ttu-id="e783f-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e783f-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e783f-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e783f-137">End of server support</span></span><br/>    | <span data-ttu-id="e783f-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e783f-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e783f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e783f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e783f-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e783f-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e783f-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="e783f-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e783f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e783f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e783f-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e783f-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e783f-145">IID</span><span class="sxs-lookup"><span data-stu-id="e783f-145">IID</span></span><br/>                      | <span data-ttu-id="e783f-146">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e783f-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e783f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e783f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e783f-148">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e783f-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
