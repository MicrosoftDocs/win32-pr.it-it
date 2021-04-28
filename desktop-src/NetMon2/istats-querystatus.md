---
description: 'Metodo IStats::QueryStatus: il metodo QueryStatus recupera lo stato di NPP.'
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: Metodo IStats::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7587c2fff56d305c0298948bdf8690fd801f3f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113479"
---
# <a name="istatsquerystatus-method"></a><span data-ttu-id="d5479-103">Metodo IStats::QueryStatus</span><span class="sxs-lookup"><span data-stu-id="d5479-103">IStats::QueryStatus method</span></span>

<span data-ttu-id="d5479-104">Il **metodo QueryStatus** recupera lo stato di NPP.</span><span class="sxs-lookup"><span data-stu-id="d5479-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5479-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5479-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d5479-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5479-107">*pNetworkStatus* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d5479-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5479-108">Puntatore a una struttura [NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del servizio NPP.</span><span class="sxs-lookup"><span data-stu-id="d5479-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="d5479-109">È responsabilità dell'applicazione allocare e liberare la memoria per la **struttura NETWORKSTATUS.**</span><span class="sxs-lookup"><span data-stu-id="d5479-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5479-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5479-110">Return value</span></span>

<span data-ttu-id="d5479-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d5479-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d5479-112">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="d5479-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="d5479-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5479-113">Return code</span></span>                                                                                              | <span data-ttu-id="d5479-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5479-114">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5479-115"><dt>**PARAMETRO NON \_ VALIDO DI NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5479-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="d5479-116">Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida.</span><span class="sxs-lookup"><span data-stu-id="d5479-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="d5479-117">Allocare memoria per questa struttura e chiamare nuovamente il **metodo IStats::QueryStatus.**</span><span class="sxs-lookup"><span data-stu-id="d5479-117">Allocate memory for this structure and call the **IStats::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5479-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5479-118">Remarks</span></span>

<span data-ttu-id="d5479-119">Questo metodo può essere chiamato in qualsiasi momento dopo la [chiamata del metodo CreateNPPInterface.](createnppinterface.md)</span><span class="sxs-lookup"><span data-stu-id="d5479-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="d5479-120">Può essere chiamato per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono in sospeso trigger.</span><span class="sxs-lookup"><span data-stu-id="d5479-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="d5479-121">Prima di chiamare questo metodo, tuttavia, è necessario allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="d5479-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5479-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5479-122">Requirements</span></span>



| <span data-ttu-id="d5479-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5479-123">Requirement</span></span> | <span data-ttu-id="d5479-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d5479-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5479-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5479-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d5479-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5479-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d5479-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5479-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d5479-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d5479-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d5479-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5479-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5479-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="d5479-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d5479-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d5479-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5479-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5479-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5479-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5479-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5479-134">IStat</span><span class="sxs-lookup"><span data-stu-id="d5479-134">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="d5479-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="d5479-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="d5479-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="d5479-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




