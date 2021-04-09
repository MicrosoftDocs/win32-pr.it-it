---
description: Il \_ metodo di autenticazione ICC consente a un'applicazione di autenticare la smart card.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'Metodo ISCardAuth:: ICC_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966628"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="8663f-103">Metodo di autenticazione ISCardAuth:: ICC \_</span><span class="sxs-lookup"><span data-stu-id="8663f-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="8663f-104">\[Il metodo di **\_ autenticazione ICC** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8663f-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8663f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8663f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8663f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8663f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8663f-107">Il metodo di **\_ autenticazione ICC** consente a un'applicazione di autenticare la smart card.</span><span class="sxs-lookup"><span data-stu-id="8663f-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="8663f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8663f-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8663f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8663f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8663f-110">*lAlgoID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8663f-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8663f-111">Algoritmo da usare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8663f-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8663f-112">*pParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8663f-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8663f-113">Oggetto [**IByteBuffer**](ibytebuffer.md) che contiene i parametri specifici del fornitore del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8663f-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8663f-114">*pbuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8663f-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8663f-115">In input contiene i dati da utilizzare nel processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8663f-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="8663f-116">Nell'output, contiene il risultato del processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8663f-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8663f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8663f-117">Return value</span></span>

<span data-ttu-id="8663f-118">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8663f-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8663f-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8663f-119">Return code</span></span>                                                                                   | <span data-ttu-id="8663f-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8663f-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8663f-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8663f-122">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8663f-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8663f-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8663f-124">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="8663f-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8663f-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8663f-126">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="8663f-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8663f-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8663f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8663f-128">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8663f-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8663f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="8663f-129">Remarks</span></span>

<span data-ttu-id="8663f-130">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="8663f-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="8663f-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8663f-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8663f-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8663f-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8663f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8663f-133">Requirements</span></span>



| <span data-ttu-id="8663f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8663f-134">Requirement</span></span> | <span data-ttu-id="8663f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8663f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8663f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8663f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8663f-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8663f-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8663f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8663f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8663f-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8663f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8663f-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8663f-140">End of client support</span></span><br/>    | <span data-ttu-id="8663f-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8663f-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8663f-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8663f-142">End of server support</span></span><br/>    | <span data-ttu-id="8663f-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8663f-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8663f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8663f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8663f-145">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="8663f-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
