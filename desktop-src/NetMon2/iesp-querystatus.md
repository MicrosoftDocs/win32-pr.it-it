---
description: Recupera lo stato di NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'Metodo IESP:: QueryStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226967"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="33bb9-103">Metodo IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="33bb9-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="33bb9-104">Il metodo **QueryStatus** recupera lo stato di NPP.</span><span class="sxs-lookup"><span data-stu-id="33bb9-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="33bb9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33bb9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="33bb9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33bb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33bb9-107">*pNetworkStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33bb9-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33bb9-108">Puntatore a una struttura [NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, pausa, arresto e così via) dell'oggetto NPP.</span><span class="sxs-lookup"><span data-stu-id="33bb9-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="33bb9-109">L'utente deve allocare e liberare la memoria per la struttura NETWORKSTATUS.</span><span class="sxs-lookup"><span data-stu-id="33bb9-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33bb9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33bb9-110">Return value</span></span>

<span data-ttu-id="33bb9-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="33bb9-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="33bb9-112">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="33bb9-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="33bb9-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33bb9-113">Return code</span></span>                                                                                              | <span data-ttu-id="33bb9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33bb9-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="33bb9-115"><dt>**\_parametro NMERR non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="33bb9-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="33bb9-116">Il parametro *pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida.</span><span class="sxs-lookup"><span data-stu-id="33bb9-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="33bb9-117">Allocare memoria per questa struttura e chiamare di nuovo **IESP:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="33bb9-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33bb9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="33bb9-118">Remarks</span></span>

<span data-ttu-id="33bb9-119">Questo metodo può essere chiamato in qualsiasi momento dopo la chiamata di [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="33bb9-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="33bb9-120">È possibile chiamare questo metodo per verificare se l'oggetto NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono presenti trigger in sospeso.</span><span class="sxs-lookup"><span data-stu-id="33bb9-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="33bb9-121">Prima di chiamare questo metodo, allocare la memoria richiesta per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="33bb9-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="33bb9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33bb9-122">Requirements</span></span>



| <span data-ttu-id="33bb9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="33bb9-123">Requirement</span></span> | <span data-ttu-id="33bb9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="33bb9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bb9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33bb9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33bb9-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33bb9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="33bb9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33bb9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33bb9-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33bb9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="33bb9-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33bb9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bb9-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="33bb9-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="33bb9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="33bb9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33bb9-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33bb9-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bb9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33bb9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bb9-134">IESP</span><span class="sxs-lookup"><span data-stu-id="33bb9-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="33bb9-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="33bb9-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="33bb9-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="33bb9-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




