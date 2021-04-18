---
description: Il metodo GetRange recupera l'intervallo di valori validi per una determinata proprietà del dispositivo audio.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'Metodo ITAudioDeviceControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325457"
---
# <a name="itaudiodevicecontrolgetrange-method"></a><span data-ttu-id="19ff6-103">Metodo ITAudioDeviceControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="19ff6-103">ITAudioDeviceControl::GetRange method</span></span>

<span data-ttu-id="19ff6-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="19ff6-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="19ff6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="19ff6-106">Il metodo **GetRange** recupera l'intervallo di valori validi per una determinata [**proprietà del dispositivo audio**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="19ff6-106">The **GetRange** method retrieves the range of valid values for a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="19ff6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19ff6-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="19ff6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19ff6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ff6-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-110">Membro dell'enumerazione [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="19ff6-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-111">*plMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-112">Valore minimo valido per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="19ff6-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-113">*plMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-114">Valore valido massimo per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="19ff6-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-115">*plSteppingDelta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-116">Incremento in base al quale è possibile aumentare o diminuire il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="19ff6-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-117">*plDefault* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-118">Valore predefinito per il parametro *Property* .</span><span class="sxs-lookup"><span data-stu-id="19ff6-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="19ff6-119">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19ff6-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19ff6-120">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="19ff6-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ff6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19ff6-121">Return value</span></span>

<span data-ttu-id="19ff6-122">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="19ff6-122">This method can return one of these values.</span></span>



| <span data-ttu-id="19ff6-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="19ff6-123">Return code</span></span>                                                                                   | <span data-ttu-id="19ff6-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19ff6-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="19ff6-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19ff6-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="19ff6-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="19ff6-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19ff6-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="19ff6-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="19ff6-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="19ff6-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19ff6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19ff6-129">Requirements</span></span>



| <span data-ttu-id="19ff6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ff6-130">Requirement</span></span> | <span data-ttu-id="19ff6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="19ff6-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19ff6-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="19ff6-132">TAPI version</span></span><br/> | <span data-ttu-id="19ff6-133">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="19ff6-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="19ff6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19ff6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="19ff6-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ff6-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="19ff6-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="19ff6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="19ff6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19ff6-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="19ff6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="19ff6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="19ff6-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ff6-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19ff6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19ff6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ff6-141">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="19ff6-141">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="19ff6-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="19ff6-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="19ff6-143">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="19ff6-143">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




