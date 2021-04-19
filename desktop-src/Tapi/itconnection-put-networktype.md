---
description: Il \_ metodo Put NetworkType imposta il tipo di rete.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: 'ITConnection: metodo:p ut_NetworkType (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326498"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="6b7a4-103">ITConnection::p UT \_ NetworkType metodo</span><span class="sxs-lookup"><span data-stu-id="6b7a4-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="6b7a4-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b7a4-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="6b7a4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6b7a4-106">Il metodo **put \_ NetworkType** imposta il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b7a4-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="6b7a4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b7a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7a4-109">*pNetworkType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b7a4-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b7a4-110">Puntatore a un **BSTR** che contiene il tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b7a4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b7a4-111">Return value</span></span>

<span data-ttu-id="6b7a4-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6b7a4-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6b7a4-113">Return code</span></span>                                                                                   | <span data-ttu-id="6b7a4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b7a4-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6b7a4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6b7a4-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6b7a4-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6b7a4-118">Il parametro *pNetworkType* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="6b7a4-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b7a4-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6b7a4-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6b7a4-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6b7a4-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6b7a4-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6b7a4-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b7a4-125">Remarks</span></span>

<span data-ttu-id="6b7a4-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PNetworkType* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="6b7a4-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7a4-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b7a4-127">Requirements</span></span>



| <span data-ttu-id="6b7a4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b7a4-128">Requirement</span></span> | <span data-ttu-id="6b7a4-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6b7a4-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7a4-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6b7a4-130">TAPI version</span></span><br/> | <span data-ttu-id="6b7a4-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6b7a4-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6b7a4-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b7a4-132">Header</span></span><br/>       | <dl> <span data-ttu-id="6b7a4-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b7a4-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b7a4-134">Library</span></span><br/>      | <dl> <span data-ttu-id="6b7a4-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6b7a4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6b7a4-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="6b7a4-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b7a4-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7a4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b7a4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7a4-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="6b7a4-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="6b7a4-140">**ITConnection:: Get \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="6b7a4-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

