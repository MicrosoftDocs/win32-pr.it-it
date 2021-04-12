---
description: Il metodo DoConfigure deve essere implementato dal monitoraggio. MCSVC chiama questo metodo per ottenere le informazioni di configurazione per l'acquisizione.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: Metodo IMonitor::D oConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128915"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="99b0b-104">IMonitor::D Metodo oConfigure</span><span class="sxs-lookup"><span data-stu-id="99b0b-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="99b0b-105">Il metodo **DoConfigure** deve essere implementato dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="99b0b-106">MCSVC chiama questo metodo per ottenere le informazioni di configurazione per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="99b0b-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b0b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99b0b-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="99b0b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="99b0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b0b-109">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b0b-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b0b-110">Nome di un'istanza del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="99b0b-111">*pConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99b0b-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b0b-112">Stringa di configurazione fornita da MCSVC.</span><span class="sxs-lookup"><span data-stu-id="99b0b-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="99b0b-113">Il monitoraggio deve analizzare questa stringa per i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="99b0b-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="99b0b-114">*ppScriptInstance* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="99b0b-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b0b-115">Indirizzo della stringa HTML utilizzata per configurare il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="99b0b-116">Se per la configurazione viene utilizzato uno script predefinito, questo valore deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="99b0b-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b0b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99b0b-117">Return value</span></span>

<span data-ttu-id="99b0b-118">Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR) e MCSVC eseguirà il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="99b0b-119">Se il metodo ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="99b0b-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="99b0b-120">Il valore restituito di NMERR \_ Monitor \_ config \_ failed è accettabile, ma quando viene restituito questo errore non è possibile avviare il monitoraggio fino a quando non viene eseguita una futura chiamata **DoConfigure** .</span><span class="sxs-lookup"><span data-stu-id="99b0b-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="99b0b-121">Qualsiasi altro errore impedisce l'attivazione dell'istanza del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b0b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="99b0b-122">Remarks</span></span>

<span data-ttu-id="99b0b-123">MCSVC chiama questo metodo dopo che è stato connesso alla rete e prima che venga chiamato il metodo [IRTC:: Configure](irtc-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="99b0b-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="99b0b-124">Il monitoraggio può archiviare le informazioni fornite da questa chiamata, aggiornare lo script HTML o la stringa di configurazione e impostare il [filtro di acquisizione](capture-filters.md) nel BLOB di NPP.</span><span class="sxs-lookup"><span data-stu-id="99b0b-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="99b0b-125">MCSVC può chiamare questo metodo più volte, ma non può essere chiamato durante l'acquisizione dei dati da parte del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="99b0b-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="99b0b-126">Si noti che ogni volta che un [NPP](network-packet-providers.md) avvia un'acquisizione, la connessione alla rete deve essere configurata.</span><span class="sxs-lookup"><span data-stu-id="99b0b-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="99b0b-127">Questa restrizione include le situazioni in cui il NPP inizia e arresta la stessa acquisizione.</span><span class="sxs-lookup"><span data-stu-id="99b0b-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b0b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99b0b-128">Requirements</span></span>



| <span data-ttu-id="99b0b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b0b-129">Requirement</span></span> | <span data-ttu-id="99b0b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="99b0b-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99b0b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b0b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="99b0b-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99b0b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="99b0b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b0b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="99b0b-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99b0b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99b0b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99b0b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b0b-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b0b-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




