---
description: Il metodo Get recupera il valore di una proprietà di impostazione audio specificata.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'Metodo ITAudioSettings:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331600"
---
# <a name="itaudiosettingsget-method"></a><span data-ttu-id="0493a-103">Metodo ITAudioSettings:: Get</span><span class="sxs-lookup"><span data-stu-id="0493a-103">ITAudioSettings::Get method</span></span>

<span data-ttu-id="0493a-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0493a-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0493a-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0493a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0493a-106">Il metodo **Get** Recupera il valore di una [**proprietà di impostazione audio**](audiosettingsproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="0493a-106">The **Get** method retrieves the value of a given [**audio setting property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0493a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0493a-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="0493a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0493a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0493a-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0493a-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0493a-110">Membro dell'enumerazione [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0493a-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="0493a-111">*plValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0493a-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0493a-112">Valore della *Proprietà* di input.</span><span class="sxs-lookup"><span data-stu-id="0493a-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="0493a-113">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0493a-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0493a-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="0493a-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0493a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0493a-115">Return value</span></span>

<span data-ttu-id="0493a-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0493a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="0493a-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0493a-117">Return code</span></span>                                                                                   | <span data-ttu-id="0493a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0493a-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0493a-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0493a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0493a-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0493a-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0493a-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0493a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0493a-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0493a-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0493a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0493a-123">Requirements</span></span>



| <span data-ttu-id="0493a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0493a-124">Requirement</span></span> | <span data-ttu-id="0493a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0493a-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0493a-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0493a-126">TAPI version</span></span><br/> | <span data-ttu-id="0493a-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0493a-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="0493a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0493a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="0493a-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0493a-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0493a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0493a-130">Library</span></span><br/>      | <dl> <span data-ttu-id="0493a-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0493a-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0493a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0493a-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="0493a-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0493a-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0493a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0493a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0493a-135">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="0493a-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="0493a-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="0493a-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="0493a-137">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="0493a-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




