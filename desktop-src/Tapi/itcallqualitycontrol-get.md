---
description: Il metodo get ottiene il valore di una determinata proprietà del controllo della qualità della chiamata.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Metodo ITCallQualityControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332006"
---
# <a name="itcallqualitycontrolget-method"></a><span data-ttu-id="d956f-103">Metodo ITCallQualityControl:: Get</span><span class="sxs-lookup"><span data-stu-id="d956f-103">ITCallQualityControl::Get method</span></span>

<span data-ttu-id="d956f-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d956f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d956f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d956f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d956f-106">Il metodo **Get** ottiene il valore di una determinata [proprietà del controllo della qualità della chiamata](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d956f-106">The **Get** method gets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d956f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d956f-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d956f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d956f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d956f-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d956f-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d956f-110">Membro dell'enumerazione [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d956f-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="d956f-111">*plValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d956f-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d956f-112">Valore della *Proprietà* di input.</span><span class="sxs-lookup"><span data-stu-id="d956f-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="d956f-113">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d956f-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d956f-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="d956f-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d956f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d956f-115">Return value</span></span>

<span data-ttu-id="d956f-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d956f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d956f-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d956f-117">Return code</span></span>                                                                                   | <span data-ttu-id="d956f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d956f-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d956f-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d956f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d956f-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d956f-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d956f-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d956f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d956f-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d956f-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d956f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d956f-123">Requirements</span></span>



| <span data-ttu-id="d956f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d956f-124">Requirement</span></span> | <span data-ttu-id="d956f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d956f-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d956f-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d956f-126">TAPI version</span></span><br/> | <span data-ttu-id="d956f-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d956f-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="d956f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d956f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="d956f-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d956f-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d956f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="d956f-130">Library</span></span><br/>      | <dl> <span data-ttu-id="d956f-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d956f-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="d956f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d956f-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="d956f-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d956f-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d956f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d956f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d956f-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="d956f-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="d956f-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="d956f-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="d956f-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="d956f-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




