---
description: Il metodo GetRange Ottiene l'intervallo di valori validi per una determinata proprietà della qualità della chiamata.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'Metodo ITCallQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328058"
---
# <a name="itcallqualitycontrolgetrange-method"></a><span data-ttu-id="efd7f-103">Metodo ITCallQualityControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="efd7f-103">ITCallQualityControl::GetRange method</span></span>

<span data-ttu-id="efd7f-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="efd7f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="efd7f-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="efd7f-106">Il metodo **GetRange** Ottiene l'intervallo di valori validi per una determinata [proprietà della qualità della chiamata](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="efd7f-106">The **GetRange** method gets the range of valid values for a given [call quality property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="efd7f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efd7f-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="efd7f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efd7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd7f-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-110">Membro dell'enumerazione [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="efd7f-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="efd7f-111">*plMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-112">Valore minimo valido per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="efd7f-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="efd7f-113">*plMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-114">Valore valido massimo per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="efd7f-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="efd7f-115">*plSteppingDelta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-116">Incremento in base al quale è possibile aumentare o diminuire il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="efd7f-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="efd7f-117">*plDefault* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-118">Valore predefinito per il parametro *Property* .</span><span class="sxs-lookup"><span data-stu-id="efd7f-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="efd7f-119">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efd7f-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efd7f-120">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="efd7f-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd7f-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efd7f-121">Return value</span></span>

<span data-ttu-id="efd7f-122">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="efd7f-122">This method can return one of these values.</span></span>



| <span data-ttu-id="efd7f-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="efd7f-123">Return code</span></span>                                                                                   | <span data-ttu-id="efd7f-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efd7f-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="efd7f-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efd7f-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="efd7f-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="efd7f-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="efd7f-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="efd7f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="efd7f-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="efd7f-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="efd7f-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efd7f-129">Requirements</span></span>



| <span data-ttu-id="efd7f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="efd7f-130">Requirement</span></span> | <span data-ttu-id="efd7f-131">Valore</span><span class="sxs-lookup"><span data-stu-id="efd7f-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efd7f-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="efd7f-132">TAPI version</span></span><br/> | <span data-ttu-id="efd7f-133">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="efd7f-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="efd7f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efd7f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="efd7f-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd7f-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="efd7f-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="efd7f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="efd7f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efd7f-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="efd7f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="efd7f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="efd7f-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efd7f-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efd7f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efd7f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd7f-141">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="efd7f-141">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="efd7f-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="efd7f-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="efd7f-143">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="efd7f-143">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




