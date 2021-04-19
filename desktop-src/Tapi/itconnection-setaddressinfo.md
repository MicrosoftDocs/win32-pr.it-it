---
description: Il metodo SetAddressInfo imposta le informazioni sull'indirizzo.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Metodo ITConnection:: SetAddressInfo (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326497"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="2694d-103">Metodo ITConnection:: SetAddressInfo</span><span class="sxs-lookup"><span data-stu-id="2694d-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="2694d-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2694d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2694d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="2694d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2694d-106">Il metodo **SetAddressInfo** imposta le informazioni sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="2694d-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2694d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2694d-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="2694d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2694d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2694d-109">*pStartAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2694d-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2694d-110">Puntatore a un **BSTR** che contiene l'indirizzo iniziale.</span><span class="sxs-lookup"><span data-stu-id="2694d-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="2694d-111">*NumAddresses* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2694d-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2694d-112">Numero di indirizzi da utilizzare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="2694d-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="2694d-113">Valore *TTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2694d-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2694d-114">ambito TTL ( [*time to Live*](t-tapgloss.md) ) per le trasmissioni sugli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="2694d-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2694d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2694d-115">Return value</span></span>

<span data-ttu-id="2694d-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2694d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2694d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2694d-117">Value</span></span>                                                                                         | <span data-ttu-id="2694d-118">Significato</span><span class="sxs-lookup"><span data-stu-id="2694d-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2694d-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2694d-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2694d-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="2694d-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2694d-122">Il parametro *pStartAddress*, *NumAddresses* o *TTL* non è valido.</span><span class="sxs-lookup"><span data-stu-id="2694d-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="2694d-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2694d-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2694d-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="2694d-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2694d-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2694d-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="2694d-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2694d-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="2694d-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="2694d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2694d-129">Remarks</span></span>

<span data-ttu-id="2694d-130">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PStartAddress* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="2694d-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2694d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2694d-131">Requirements</span></span>



| <span data-ttu-id="2694d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2694d-132">Requirement</span></span> | <span data-ttu-id="2694d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2694d-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2694d-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="2694d-134">TAPI version</span></span><br/> | <span data-ttu-id="2694d-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2694d-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2694d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2694d-136">Header</span></span><br/>       | <dl> <span data-ttu-id="2694d-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2694d-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="2694d-138">Library</span></span><br/>      | <dl> <span data-ttu-id="2694d-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2694d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2694d-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="2694d-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2694d-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2694d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2694d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2694d-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="2694d-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

