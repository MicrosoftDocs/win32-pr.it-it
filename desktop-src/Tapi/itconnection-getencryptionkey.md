---
description: Il metodo GetEncryptionKey ottiene la chiave di crittografia.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Metodo ITConnection:: GetEncryptionKey (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326501"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="f33b0-103">Metodo ITConnection:: GetEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f33b0-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="f33b0-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f33b0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f33b0-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f33b0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f33b0-106">Il metodo **GetEncryptionKey** ottiene la chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f33b0-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f33b0-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="f33b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f33b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33b0-109">*ppKeyType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f33b0-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33b0-110">Puntatore a un **BSTR** che contiene il tipo di chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f33b0-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="f33b0-111">*pfValidKeyData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f33b0-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33b0-112">Indica la validità dei dati della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f33b0-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="f33b0-113">*ppKeyData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f33b0-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33b0-114">Puntatore a un **BSTR** che contiene i dati della chiave di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f33b0-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33b0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f33b0-115">Return value</span></span>

<span data-ttu-id="f33b0-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f33b0-116">This method can return one of these values.</span></span>



| <span data-ttu-id="f33b0-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f33b0-117">Return code</span></span>                                                                                   | <span data-ttu-id="f33b0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f33b0-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f33b0-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f33b0-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f33b0-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="f33b0-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f33b0-122">Il parametro *ppKeyType, pfValidKeyData* o *ppKeyData* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="f33b0-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="f33b0-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f33b0-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f33b0-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="f33b0-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f33b0-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f33b0-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="f33b0-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f33b0-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="f33b0-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="f33b0-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f33b0-129">Remarks</span></span>

<span data-ttu-id="f33b0-130">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per i parametri *ppKeyType* e *ppKeyData* .</span><span class="sxs-lookup"><span data-stu-id="f33b0-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33b0-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f33b0-131">Requirements</span></span>



| <span data-ttu-id="f33b0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33b0-132">Requirement</span></span> | <span data-ttu-id="f33b0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f33b0-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f33b0-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f33b0-134">TAPI version</span></span><br/> | <span data-ttu-id="f33b0-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f33b0-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f33b0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f33b0-136">Header</span></span><br/>       | <dl> <span data-ttu-id="f33b0-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f33b0-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="f33b0-138">Library</span></span><br/>      | <dl> <span data-ttu-id="f33b0-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f33b0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f33b0-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="f33b0-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33b0-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33b0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f33b0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33b0-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="f33b0-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

