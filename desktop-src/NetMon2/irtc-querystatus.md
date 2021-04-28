---
description: 'Metodo IRTC::QueryStatus: il metodo QueryStatus recupera lo stato del NPP.'
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: Metodo IRTC::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd8c18d19df7d577ad219742520630f00122a41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110609"
---
# <a name="irtcquerystatus-method"></a><span data-ttu-id="91792-103">Metodo IRTC::QueryStatus</span><span class="sxs-lookup"><span data-stu-id="91792-103">IRTC::QueryStatus method</span></span>

<span data-ttu-id="91792-104">Il **metodo QueryStatus** recupera lo stato del NPP.</span><span class="sxs-lookup"><span data-stu-id="91792-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="91792-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91792-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="91792-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91792-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91792-107">*pNetworkStatus* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="91792-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91792-108">Puntatore a una [struttura NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del NPP.</span><span class="sxs-lookup"><span data-stu-id="91792-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="91792-109">È responsabilità dell'applicazione allocare e liberare la memoria per la **struttura NETWORKSTATUS.**</span><span class="sxs-lookup"><span data-stu-id="91792-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91792-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91792-110">Return value</span></span>

<span data-ttu-id="91792-111">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="91792-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="91792-112">Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="91792-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="91792-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="91792-113">Return code</span></span>                                                                                              | <span data-ttu-id="91792-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91792-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91792-115"><dt>**PARAMETRO NON VALIDO DI \_ NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="91792-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="91792-116">Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida.</span><span class="sxs-lookup"><span data-stu-id="91792-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="91792-117">Allocare memoria per questa struttura e chiamare **di nuovo IRTC::QueryStatus.**</span><span class="sxs-lookup"><span data-stu-id="91792-117">Allocate memory for this structure and call **IRTC::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91792-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="91792-118">Remarks</span></span>

<span data-ttu-id="91792-119">Questo metodo può essere chiamato in qualsiasi momento dopo [la chiamata del metodo CreateNPPInterface.](createnppinterface.md)</span><span class="sxs-lookup"><span data-stu-id="91792-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="91792-120">È possibile chiamare questo metodo per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono presenti trigger in sospeso.</span><span class="sxs-lookup"><span data-stu-id="91792-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="91792-121">Prima di chiamare questo metodo, tuttavia, è necessario allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="91792-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="91792-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91792-122">Requirements</span></span>



| <span data-ttu-id="91792-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="91792-123">Requirement</span></span> | <span data-ttu-id="91792-124">Valore</span><span class="sxs-lookup"><span data-stu-id="91792-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91792-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91792-125">Minimum supported client</span></span><br/> | <span data-ttu-id="91792-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91792-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="91792-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91792-127">Minimum supported server</span></span><br/> | <span data-ttu-id="91792-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91792-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="91792-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91792-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="91792-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="91792-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="91792-131">DLL</span><span class="sxs-lookup"><span data-stu-id="91792-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91792-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91792-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91792-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91792-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91792-134">IRTC</span><span class="sxs-lookup"><span data-stu-id="91792-134">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="91792-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="91792-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="91792-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="91792-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




