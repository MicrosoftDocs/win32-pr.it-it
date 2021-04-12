---
description: Recupera l'identificatore del protocollo attualmente in uso nella smart card.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Metodo IsValid:: get_Protocol (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348051"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="8286c-103">Metodo IsValid:: Get \_ Protocol</span><span class="sxs-lookup"><span data-stu-id="8286c-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="8286c-104">\[Il metodo **get \_ Protocol** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8286c-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8286c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8286c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8286c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8286c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8286c-107">Il metodo **get \_ Protocol** recupera l'identificatore del protocollo attualmente in uso nella [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8286c-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8286c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8286c-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="8286c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8286c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8286c-110">*pProtocol* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8286c-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8286c-111">Puntatore all'identificatore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="8286c-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8286c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8286c-112">Return value</span></span>

<span data-ttu-id="8286c-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8286c-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8286c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8286c-114">Return code</span></span>                                                                                  | <span data-ttu-id="8286c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8286c-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8286c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8286c-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8286c-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="8286c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8286c-119">Il parametro *pProtocol* non è valido.</span><span class="sxs-lookup"><span data-stu-id="8286c-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="8286c-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="8286c-121">Un puntatore errato è stato passato in *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="8286c-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8286c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8286c-122">Remarks</span></span>

<span data-ttu-id="8286c-123">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8286c-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8286c-124">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8286c-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8286c-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="8286c-125">Examples</span></span>

<span data-ttu-id="8286c-126">Nell'esempio seguente viene illustrato come recuperare l'identificatore del protocollo attualmente in uso nella smart card.</span><span class="sxs-lookup"><span data-stu-id="8286c-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="8286c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8286c-127">Requirements</span></span>



| <span data-ttu-id="8286c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8286c-128">Requirement</span></span> | <span data-ttu-id="8286c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8286c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8286c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8286c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8286c-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8286c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8286c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8286c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8286c-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8286c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8286c-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8286c-134">End of client support</span></span><br/>    | <span data-ttu-id="8286c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8286c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8286c-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8286c-136">End of server support</span></span><br/>    | <span data-ttu-id="8286c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8286c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8286c-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8286c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8286c-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="8286c-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8286c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="8286c-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8286c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8286c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8286c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8286c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8286c-144">IID</span><span class="sxs-lookup"><span data-stu-id="8286c-144">IID</span></span><br/>                      | <span data-ttu-id="8286c-145">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8286c-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8286c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8286c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8286c-147">**Ottieni \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="8286c-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="8286c-148">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="8286c-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="8286c-149">**ottenere il \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="8286c-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="8286c-150">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="8286c-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="8286c-151">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="8286c-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
