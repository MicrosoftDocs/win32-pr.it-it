---
description: Il \_ LoopbackMode put imposta la modalità loopback multicast.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: 'IMulticastControl: metodo:p ut_LoopbackMode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5b5e51b3814b380cc06d9c960db1a4e4b9ecb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331602"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a><span data-ttu-id="054a8-103">IMulticastControl::p UT \_ LoopbackMode metodo</span><span class="sxs-lookup"><span data-stu-id="054a8-103">IMulticastControl::put\_LoopbackMode method</span></span>

<span data-ttu-id="054a8-104">\[**Inserisci \_ LoopbackMode** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="054a8-104">\[**put\_LoopbackMode** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="054a8-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="054a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="054a8-106">Il **\_ LoopbackMode put** imposta la modalità loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="054a8-106">The **put\_LoopbackMode** sets the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="054a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="054a8-107">Syntax</span></span>


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a><span data-ttu-id="054a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="054a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="054a8-109">*modalità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="054a8-109">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="054a8-110">[**Multicast \_ \_**](multicast-loopback-mode.md) Descrittore della modalità loopback della nuova modalità loopback.</span><span class="sxs-lookup"><span data-stu-id="054a8-110">[**MULTICAST\_LOOPBACK\_MODE**](multicast-loopback-mode.md) descriptor of the new loopback mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="054a8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="054a8-111">Return value</span></span>

<span data-ttu-id="054a8-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="054a8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="054a8-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="054a8-113">Return code</span></span>                                                                                  | <span data-ttu-id="054a8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="054a8-114">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="054a8-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="054a8-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="054a8-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="054a8-116">Method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="054a8-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="054a8-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="054a8-118">Il parametro *mode* non è valido.</span><span class="sxs-lookup"><span data-stu-id="054a8-118">The *mode* parameter is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="054a8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="054a8-119">Requirements</span></span>



| <span data-ttu-id="054a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="054a8-120">Requirement</span></span> | <span data-ttu-id="054a8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="054a8-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="054a8-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="054a8-122">TAPI version</span></span><br/> | <span data-ttu-id="054a8-123">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="054a8-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="054a8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="054a8-124">Header</span></span><br/>       | <dl> <span data-ttu-id="054a8-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="054a8-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="054a8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="054a8-126">Library</span></span><br/>      | <dl> <span data-ttu-id="054a8-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="054a8-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="054a8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="054a8-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="054a8-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="054a8-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="054a8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="054a8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="054a8-131">**IMulticastControl**</span><span class="sxs-lookup"><span data-stu-id="054a8-131">**IMulticastControl**</span></span>](imulticastcontrol.md)
</dt> </dl>

 

 




