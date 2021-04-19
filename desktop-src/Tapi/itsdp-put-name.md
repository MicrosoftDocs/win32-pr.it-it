---
description: Il \_ metodo Put Name imposta il nome della sessione.
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: 'ITSdp: metodo:p ut_Name (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328057"
---
# <a name="itsdpput_name-method"></a><span data-ttu-id="b844b-103">ITSdp: \_ Metodo nome ut:p</span><span class="sxs-lookup"><span data-stu-id="b844b-103">ITSdp::put\_Name method</span></span>

<span data-ttu-id="b844b-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b844b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b844b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="b844b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b844b-106">Il metodo **put \_ Name** imposta il nome della sessione.</span><span class="sxs-lookup"><span data-stu-id="b844b-106">The **put\_Name** method sets the session name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b844b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b844b-107">Syntax</span></span>


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="b844b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b844b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b844b-109">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b844b-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b844b-110">Puntatore a un **BSTR** che contiene il nome della sessione.</span><span class="sxs-lookup"><span data-stu-id="b844b-110">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b844b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b844b-111">Return value</span></span>

<span data-ttu-id="b844b-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b844b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b844b-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b844b-113">Return code</span></span>                                                                                   | <span data-ttu-id="b844b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b844b-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b844b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b844b-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b844b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b844b-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b844b-118">Il parametro *pname* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="b844b-118">The *pName* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="b844b-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b844b-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b844b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b844b-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b844b-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b844b-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b844b-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b844b-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="b844b-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b844b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b844b-125">Remarks</span></span>

<span data-ttu-id="b844b-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *pname* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="b844b-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b844b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b844b-127">Requirements</span></span>



| <span data-ttu-id="b844b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b844b-128">Requirement</span></span> | <span data-ttu-id="b844b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b844b-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b844b-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b844b-130">TAPI version</span></span><br/> | <span data-ttu-id="b844b-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b844b-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b844b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b844b-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b844b-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b844b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="b844b-134">Library</span></span><br/>      | <dl> <span data-ttu-id="b844b-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b844b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b844b-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="b844b-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b844b-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b844b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b844b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b844b-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b844b-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="b844b-140">**ITSdp:: Get \_ nome**</span><span class="sxs-lookup"><span data-stu-id="b844b-140">**ITSdp::get\_Name**</span></span>](itsdp-get-name.md)
</dt> </dl>

 

