---
description: Il metodo di autenticazione dell'APP \_ autentica l'applicazione. Consente a un'applicazione di autenticarsi (usando un protocollo di verifica/firma) quando l'autenticazione viene richiesta da una smart card.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Metodo ISCardAuth:: APP_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880177"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="15009-104">Metodo di autenticazione ISCardAuth:: APP \_</span><span class="sxs-lookup"><span data-stu-id="15009-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="15009-105">\[Il metodo di **\_ autenticazione dell'app** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="15009-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="15009-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="15009-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="15009-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="15009-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="15009-108">Il metodo di autenticazione dell' **app \_** autentica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15009-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="15009-109">Consente a un'applicazione di autenticarsi (usando un protocollo di verifica/firma) quando l'autenticazione viene richiesta da una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="15009-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15009-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15009-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="15009-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="15009-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15009-112">*lAlgoID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15009-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15009-113">Algoritmo da usare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="15009-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="15009-114">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15009-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15009-115">Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="15009-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="15009-116">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15009-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15009-117">Dati necessari per il calcolo.</span><span class="sxs-lookup"><span data-stu-id="15009-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15009-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15009-118">Return value</span></span>

<span data-ttu-id="15009-119">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="15009-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="15009-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="15009-120">Return code</span></span>                                                                                   | <span data-ttu-id="15009-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15009-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="15009-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15009-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="15009-123">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="15009-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="15009-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="15009-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="15009-125">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="15009-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="15009-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="15009-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="15009-127">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="15009-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="15009-128"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="15009-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="15009-129">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="15009-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="15009-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="15009-130">Remarks</span></span>

<span data-ttu-id="15009-131">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="15009-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="15009-132">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="15009-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="15009-133">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="15009-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15009-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15009-134">Requirements</span></span>



| <span data-ttu-id="15009-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="15009-135">Requirement</span></span> | <span data-ttu-id="15009-136">Valore</span><span class="sxs-lookup"><span data-stu-id="15009-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15009-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15009-137">Minimum supported client</span></span><br/> | <span data-ttu-id="15009-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="15009-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="15009-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15009-139">Minimum supported server</span></span><br/> | <span data-ttu-id="15009-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15009-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="15009-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="15009-141">End of client support</span></span><br/>    | <span data-ttu-id="15009-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="15009-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="15009-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="15009-143">End of server support</span></span><br/>    | <span data-ttu-id="15009-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15009-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="15009-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15009-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15009-146">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="15009-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="15009-147">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="15009-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
