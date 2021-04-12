---
description: Recupera lo stato corrente della smart card.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'Metodo IsValid:: get_Status (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234016"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="ebd6a-103">Metodo IsValid:: Get \_ status</span><span class="sxs-lookup"><span data-stu-id="ebd6a-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="ebd6a-104">\[Il metodo **get \_ status** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ebd6a-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ebd6a-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ebd6a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ebd6a-107">Il metodo **get \_ status** recupera lo [*stato*](../secgloss/s-gly.md) corrente della [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ebd6a-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd6a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebd6a-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ebd6a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebd6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd6a-110">*pStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ebd6a-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebd6a-111">Puntatore alla variabile di stato.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebd6a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebd6a-112">Return value</span></span>

<span data-ttu-id="ebd6a-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ebd6a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ebd6a-114">Return code</span></span>                                                                                  | <span data-ttu-id="ebd6a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebd6a-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="ebd6a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ebd6a-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="ebd6a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ebd6a-119">Il parametro *pStatus* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ebd6a-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ebd6a-121">Un puntatore errato è stato passato in *pStatus*.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ebd6a-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebd6a-122">Remarks</span></span>

<span data-ttu-id="ebd6a-123">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ebd6a-124">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ebd6a-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ebd6a-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="ebd6a-125">Examples</span></span>

<span data-ttu-id="ebd6a-126">Nell'esempio seguente viene illustrato come recuperare lo stato corrente della smart card.</span><span class="sxs-lookup"><span data-stu-id="ebd6a-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="ebd6a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebd6a-127">Requirements</span></span>



| <span data-ttu-id="ebd6a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd6a-128">Requirement</span></span> | <span data-ttu-id="ebd6a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ebd6a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd6a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebd6a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd6a-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebd6a-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebd6a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebd6a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd6a-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebd6a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebd6a-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ebd6a-134">End of client support</span></span><br/>    | <span data-ttu-id="ebd6a-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebd6a-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ebd6a-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ebd6a-136">End of server support</span></span><br/>    | <span data-ttu-id="ebd6a-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebd6a-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ebd6a-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ebd6a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd6a-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="ebd6a-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ebd6a-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd6a-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebd6a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ebd6a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd6a-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd6a-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd6a-144">IID</span><span class="sxs-lookup"><span data-stu-id="ebd6a-144">IID</span></span><br/>                      | <span data-ttu-id="ebd6a-145">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ebd6a-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ebd6a-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebd6a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd6a-147">**Ottieni \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="ebd6a-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="ebd6a-148">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="ebd6a-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="ebd6a-149">**ottenere il \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="ebd6a-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="ebd6a-150">**ottenere il \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="ebd6a-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="ebd6a-151">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="ebd6a-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
