---
description: 'Metodo IDelaydC::QueryStatus: il metodo QueryStatus recupera lo stato del NPP.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: Metodo IDelaydC::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118459"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="805cf-103">Metodo IDelaydC::QueryStatus</span><span class="sxs-lookup"><span data-stu-id="805cf-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="805cf-104">Il **metodo QueryStatus** recupera lo stato del NPP.</span><span class="sxs-lookup"><span data-stu-id="805cf-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="805cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="805cf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="805cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="805cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805cf-107">*pNetworkStatus* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="805cf-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="805cf-108">Puntatore a una [struttura NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del NPP.</span><span class="sxs-lookup"><span data-stu-id="805cf-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="805cf-109">È responsabilità dell'utente allocare e liberare la memoria associata alla **struttura NETWORKSTATUS.**</span><span class="sxs-lookup"><span data-stu-id="805cf-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805cf-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="805cf-110">Return value</span></span>

<span data-ttu-id="805cf-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="805cf-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="805cf-112">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="805cf-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="805cf-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="805cf-113">Return code</span></span>                                                                                              | <span data-ttu-id="805cf-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="805cf-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="805cf-115"><dt>**PARAMETRO NON VALIDO DI \_ \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="805cf-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="805cf-116">Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida.</span><span class="sxs-lookup"><span data-stu-id="805cf-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="805cf-117">Allocare memoria per questa struttura e chiamare di nuovo il metodo **IDelaydC::QueryStatus.**</span><span class="sxs-lookup"><span data-stu-id="805cf-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="805cf-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="805cf-118">Remarks</span></span>

<span data-ttu-id="805cf-119">Questo metodo può essere chiamato in qualsiasi momento dopo [la chiamata a CreateNPPInterface.](createnppinterface.md)</span><span class="sxs-lookup"><span data-stu-id="805cf-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="805cf-120">Può essere chiamato per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono presenti trigger in sospeso.</span><span class="sxs-lookup"><span data-stu-id="805cf-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="805cf-121">Prima di chiamare questo metodo, è necessario allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="805cf-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="805cf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="805cf-122">Requirements</span></span>



| <span data-ttu-id="805cf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="805cf-123">Requirement</span></span> | <span data-ttu-id="805cf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="805cf-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805cf-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="805cf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="805cf-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="805cf-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="805cf-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="805cf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="805cf-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="805cf-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="805cf-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="805cf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="805cf-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="805cf-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="805cf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="805cf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805cf-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805cf-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805cf-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="805cf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805cf-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="805cf-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="805cf-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="805cf-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="805cf-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="805cf-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




