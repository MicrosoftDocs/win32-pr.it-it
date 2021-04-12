---
description: Il metodo getchallenge restituisce una richiesta di verifica da parte della smart card.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'Metodo ISCardAuth:: getchallenge'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226603"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="8bfb9-103">Metodo ISCardAuth:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="8bfb9-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="8bfb9-104">\[Il metodo **getchallenge** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8bfb9-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8bfb9-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8bfb9-107">Il metodo **getchallenge** restituisce una richiesta di verifica da parte della [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8bfb9-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8bfb9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bfb9-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8bfb9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bfb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bfb9-110">*lAlgoID* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfb9-111">Algoritmo da usare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8bfb9-112">*lLengthOfChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfb9-113">Lunghezza massima della risposta prevista.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="8bfb9-114">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfb9-115">Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8bfb9-116">*pbuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bfb9-117">In input punta al buffer.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-117">On input, points to the buffer.</span></span>

<span data-ttu-id="8bfb9-118">Nell'output, contiene i dati di richiesta della scheda.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bfb9-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bfb9-119">Return value</span></span>

<span data-ttu-id="8bfb9-120">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8bfb9-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8bfb9-121">Return code</span></span>                                                                                   | <span data-ttu-id="8bfb9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bfb9-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8bfb9-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb9-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8bfb9-124">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8bfb9-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb9-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8bfb9-126">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8bfb9-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb9-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8bfb9-128">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8bfb9-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8bfb9-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8bfb9-130">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8bfb9-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="8bfb9-131">Remarks</span></span>

<span data-ttu-id="8bfb9-132">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="8bfb9-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="8bfb9-133">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8bfb9-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8bfb9-134">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8bfb9-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bfb9-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bfb9-135">Requirements</span></span>



| <span data-ttu-id="8bfb9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bfb9-136">Requirement</span></span> | <span data-ttu-id="8bfb9-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8bfb9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bfb9-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bfb9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8bfb9-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8bfb9-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bfb9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8bfb9-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bfb9-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8bfb9-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8bfb9-142">End of client support</span></span><br/>    | <span data-ttu-id="8bfb9-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8bfb9-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8bfb9-144">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8bfb9-144">End of server support</span></span><br/>    | <span data-ttu-id="8bfb9-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8bfb9-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8bfb9-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bfb9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bfb9-147">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="8bfb9-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
