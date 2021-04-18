---
description: Il \_ metodo Get LoopbackMode ottiene la modalità loopback multicast.
ms.assetid: 2499c108-f70b-4afe-aa2b-2376c95b84bd
title: 'Metodo IMulticastControl:: get_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 203d68f5b620ddf5e5ce7a36e4f8b85820deab2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327409"
---
# <a name="imulticastcontrolget_loopbackmode-method"></a><span data-ttu-id="db7be-103">Metodo IMulticastControl:: Get \_ LoopbackMode</span><span class="sxs-lookup"><span data-stu-id="db7be-103">IMulticastControl::get\_LoopbackMode method</span></span>

<span data-ttu-id="db7be-104">\[**ottenere \_ LoopbackMode** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db7be-104">\[**get\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db7be-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="db7be-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="db7be-106">Il metodo **get \_ LoopbackMode** ottiene la modalità loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="db7be-106">The **get\_LoopbackMode** method gets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db7be-107">Syntax</span></span>


```C++
HRESULT get_LoopbackMode(
  [out] MULTICAST_LOOPBACK_MODE *pMode
);
```



## <a name="parameters"></a><span data-ttu-id="db7be-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db7be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7be-109">*pmode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="db7be-109">*pMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db7be-110">Puntatore al descrittore della [**\_ \_ modalità loopback multicast**](multicast-loopback-mode.md) della modalità loopback corrente.</span><span class="sxs-lookup"><span data-stu-id="db7be-110">Pointer to the [**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the current loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7be-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db7be-111">Return value</span></span>

<span data-ttu-id="db7be-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="db7be-112">This method can return one of these values.</span></span>



| <span data-ttu-id="db7be-113">Valore</span><span class="sxs-lookup"><span data-stu-id="db7be-113">Value</span></span>                                                                                        | <span data-ttu-id="db7be-114">Significato</span><span class="sxs-lookup"><span data-stu-id="db7be-114">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="db7be-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db7be-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="db7be-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="db7be-116">Method succeeded.</span></span><br/>                   |
| <dl> <span data-ttu-id="db7be-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="db7be-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="db7be-118">Il parametro *pmode* non è valido.</span><span class="sxs-lookup"><span data-stu-id="db7be-118">The *pMode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="db7be-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db7be-119">Requirements</span></span>



| <span data-ttu-id="db7be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="db7be-120">Requirement</span></span> | <span data-ttu-id="db7be-121">Valore</span><span class="sxs-lookup"><span data-stu-id="db7be-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db7be-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="db7be-122">TAPI version</span></span><br/> | <span data-ttu-id="db7be-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="db7be-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="db7be-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db7be-124">Header</span></span><br/>       | <dl> <span data-ttu-id="db7be-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7be-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="db7be-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="db7be-126">Library</span></span><br/>      | <dl> <span data-ttu-id="db7be-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db7be-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="db7be-128">DLL</span><span class="sxs-lookup"><span data-stu-id="db7be-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="db7be-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db7be-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="db7be-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db7be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7be-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="db7be-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




