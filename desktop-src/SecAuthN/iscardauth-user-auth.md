---
description: Il \_ metodo di autenticazione utente consente l'accesso ai servizi di autenticazione utente.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'Metodo ISCardAuth:: User_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879050"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="14a11-103">Metodo ISCardAuth:: User \_ AUTH</span><span class="sxs-lookup"><span data-stu-id="14a11-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="14a11-104">\[Il metodo di **\_ autenticazione utente** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="14a11-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14a11-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="14a11-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14a11-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="14a11-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="14a11-107">Il **metodo \_ di autenticazione utente** consente l'accesso ai servizi di autenticazione utente.</span><span class="sxs-lookup"><span data-stu-id="14a11-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a11-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14a11-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="14a11-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="14a11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a11-110">*lAlgorID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14a11-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a11-111">Algoritmo da usare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="14a11-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="14a11-112">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14a11-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a11-113">Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="14a11-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="14a11-114">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14a11-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a11-115">Dati da utilizzare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="14a11-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a11-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14a11-116">Return value</span></span>

<span data-ttu-id="14a11-117">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="14a11-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="14a11-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="14a11-118">Return code</span></span>                                                                                   | <span data-ttu-id="14a11-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14a11-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="14a11-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14a11-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="14a11-121">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="14a11-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="14a11-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14a11-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="14a11-123">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="14a11-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="14a11-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="14a11-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="14a11-125">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="14a11-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="14a11-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="14a11-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="14a11-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="14a11-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="14a11-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="14a11-128">Remarks</span></span>

<span data-ttu-id="14a11-129">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="14a11-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="14a11-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="14a11-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="14a11-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="14a11-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14a11-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14a11-132">Requirements</span></span>



| <span data-ttu-id="14a11-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a11-133">Requirement</span></span> | <span data-ttu-id="14a11-134">Valore</span><span class="sxs-lookup"><span data-stu-id="14a11-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14a11-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14a11-135">Minimum supported client</span></span><br/> | <span data-ttu-id="14a11-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14a11-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="14a11-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14a11-137">Minimum supported server</span></span><br/> | <span data-ttu-id="14a11-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14a11-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="14a11-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="14a11-139">End of client support</span></span><br/>    | <span data-ttu-id="14a11-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="14a11-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="14a11-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="14a11-141">End of server support</span></span><br/>    | <span data-ttu-id="14a11-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14a11-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="14a11-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14a11-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a11-144">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="14a11-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="14a11-145">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="14a11-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
