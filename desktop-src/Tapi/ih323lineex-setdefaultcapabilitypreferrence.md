---
description: Configura la preferenza delle funzionalità predefinite.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'Metodo IH323LineEx:: SetDefaultCapabilityPreferrence (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326148"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="3494e-103">Metodo IH323LineEx:: SetDefaultCapabilityPreferrence</span><span class="sxs-lookup"><span data-stu-id="3494e-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="3494e-104">\[**SetDefaultCapabilityPreferrence** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3494e-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3494e-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3494e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3494e-106">Il metodo **SetDefaultCapabilityPreferrence** configura la preferenza delle funzionalità predefinite.</span><span class="sxs-lookup"><span data-stu-id="3494e-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="3494e-107">Le funzionalità hanno un peso predefinito di 100.</span><span class="sxs-lookup"><span data-stu-id="3494e-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="3494e-108">Se l'applicazione specifica un peso maggiore per una funzionalità, avrà una priorità maggiore durante la negoziazione H. 245.</span><span class="sxs-lookup"><span data-stu-id="3494e-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="3494e-109">Se l'applicazione imposta il peso di una funzionalità su 0, non verrà utilizzata nella negoziazione H. 245.</span><span class="sxs-lookup"><span data-stu-id="3494e-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="3494e-110">Questo metodo è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="3494e-110">This method is cumulative.</span></span> <span data-ttu-id="3494e-111">Se, ad esempio, questo metodo viene chiamato per primo per disabilitare una funzionalità e viene chiamato di nuovo per disabilitarne un altro, entrambe le funzionalità verranno disabilitate come risultato di queste due chiamate.</span><span class="sxs-lookup"><span data-stu-id="3494e-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="3494e-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3494e-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="3494e-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="3494e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3494e-114">*dwNumCaps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3494e-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3494e-115">Valore **DWORD** che contiene il numero di funzionalità impostate con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3494e-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="3494e-116">*pCapabilities* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3494e-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3494e-117">Matrice di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3494e-117">An array of capabilities.</span></span> <span data-ttu-id="3494e-118">Ogni elemento della matrice è un valore [**della \_ funzionalità h245**](h245-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="3494e-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="3494e-119">*pWeights* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3494e-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3494e-120">Matrice di pesi associati alle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3494e-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3494e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3494e-121">Return value</span></span>

<span data-ttu-id="3494e-122">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3494e-122">This method can return one of these values.</span></span>



| <span data-ttu-id="3494e-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3494e-123">Return code</span></span>                                                                                   | <span data-ttu-id="3494e-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3494e-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3494e-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3494e-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3494e-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="3494e-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3494e-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3494e-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="3494e-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3494e-130">Il parametro *pCapabilities* è **null** o il parametro *PWeights* è **null** oppure sia *pCapabilities* che *PWeights* sono **null** oppure la matrice pCapabilities contiene un oggetto funzionalità H. 245 non valido.</span><span class="sxs-lookup"><span data-stu-id="3494e-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="3494e-131"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3494e-132">Impossibile leggere un elemento della matrice *pWeights* o un elemento della matrice *pCapabilities* .</span><span class="sxs-lookup"><span data-stu-id="3494e-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3494e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3494e-133">Requirements</span></span>



| <span data-ttu-id="3494e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3494e-134">Requirement</span></span> | <span data-ttu-id="3494e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3494e-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3494e-136">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3494e-136">TAPI version</span></span><br/> | <span data-ttu-id="3494e-137">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3494e-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3494e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3494e-138">Header</span></span><br/>       | <dl> <span data-ttu-id="3494e-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="3494e-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="3494e-140">Library</span></span><br/>      | <dl> <span data-ttu-id="3494e-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3494e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3494e-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="3494e-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3494e-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




