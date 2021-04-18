---
description: Il metodo set imposta il valore di una determinata proprietà del dispositivo audio.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Metodo ITAudioDeviceControl:: set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325594"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="6c9bf-103">Metodo ITAudioDeviceControl:: set</span><span class="sxs-lookup"><span data-stu-id="6c9bf-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="6c9bf-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c9bf-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="6c9bf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6c9bf-106">Il metodo **set** imposta il valore di una determinata [**proprietà del dispositivo audio**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="6c9bf-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9bf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c9bf-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="6c9bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c9bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9bf-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6c9bf-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c9bf-110">Membro dell'enumerazione [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6c9bf-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="6c9bf-111">*lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c9bf-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c9bf-112">Valore desiderato per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="6c9bf-113">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c9bf-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c9bf-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="6c9bf-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c9bf-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c9bf-115">Return value</span></span>

<span data-ttu-id="6c9bf-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-116">This method can return one of these values.</span></span>



| <span data-ttu-id="6c9bf-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6c9bf-117">Return code</span></span>                                                                                   | <span data-ttu-id="6c9bf-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c9bf-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6c9bf-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6c9bf-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6c9bf-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6c9bf-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6c9bf-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c9bf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c9bf-123">Requirements</span></span>



| <span data-ttu-id="6c9bf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c9bf-124">Requirement</span></span> | <span data-ttu-id="6c9bf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6c9bf-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9bf-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6c9bf-126">TAPI version</span></span><br/> | <span data-ttu-id="6c9bf-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6c9bf-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="6c9bf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c9bf-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6c9bf-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c9bf-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c9bf-130">Library</span></span><br/>      | <dl> <span data-ttu-id="6c9bf-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6c9bf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6c9bf-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="6c9bf-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c9bf-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9bf-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c9bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9bf-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="6c9bf-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="6c9bf-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="6c9bf-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




