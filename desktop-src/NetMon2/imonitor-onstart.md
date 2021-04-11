---
description: Il metodo OnStart è un metodo facoltativo che può essere implementato dal monitoraggio. MCSVC chiama questo metodo per richiedere che il monitoraggio avvii l'acquisizione.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Metodo IMonitor:: OnStart (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128323"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="ac630-104">Metodo IMonitor:: OnStart</span><span class="sxs-lookup"><span data-stu-id="ac630-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="ac630-105">Il metodo **OnStart** è un metodo facoltativo che può essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ac630-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="ac630-106">MCSVC chiama questo metodo per richiedere che il monitoraggio avvii l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ac630-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac630-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac630-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="ac630-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac630-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac630-109">*pUnkNPP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac630-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac630-110">Puntatore [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) all'interfaccia [IRTC](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="ac630-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="ac630-111">Il monitoraggio può utilizzare questa interfaccia per ottenere statistiche che possono essere utilizzate per determinare se l'acquisizione deve essere avviata.</span><span class="sxs-lookup"><span data-stu-id="ac630-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac630-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac630-112">Return value</span></span>

<span data-ttu-id="ac630-113">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).</span><span class="sxs-lookup"><span data-stu-id="ac630-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="ac630-114">Quando \_ viene restituito S OK, MCSVC chiama il metodo [IRTC:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="ac630-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="ac630-115">Se il metodo ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ac630-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="ac630-116">Il MCSVC non avvierà l'acquisizione se viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ac630-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac630-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac630-117">Remarks</span></span>

<span data-ttu-id="ac630-118">MCSVC chiama questo metodo prima di chiamare il metodo [IRTC:: Start](irtc-start.md) di NPP per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ac630-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac630-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac630-119">Requirements</span></span>



| <span data-ttu-id="ac630-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac630-120">Requirement</span></span> | <span data-ttu-id="ac630-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ac630-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac630-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac630-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac630-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac630-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ac630-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac630-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac630-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac630-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ac630-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac630-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac630-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac630-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac630-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac630-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac630-129">IMonitor</span><span class="sxs-lookup"><span data-stu-id="ac630-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="ac630-130">Provider di pacchetti di rete</span><span class="sxs-lookup"><span data-stu-id="ac630-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

