---
description: Il metodo GetRange Ottiene l'intervallo di valori validi per una determinata proprietà di qualità del flusso.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'Metodo ITStreamQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328592"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="f2f5c-103">Metodo ITStreamQualityControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="f2f5c-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="f2f5c-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f2f5c-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f2f5c-106">Il metodo **GetRange** Ottiene l'intervallo di valori validi per una determinata [**proprietà di qualità del flusso**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f2f5c-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f5c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2f5c-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f2f5c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2f5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f5c-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-110">Membro dell'enumerazione [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f5c-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="f2f5c-111">*plMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-112">Valore minimo valido per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="f2f5c-113">*plMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-114">Valore valido massimo per la proprietà di input.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="f2f5c-115">*plSteppingDelta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-116">Incremento in base al quale è possibile aumentare o diminuire il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="f2f5c-117">*plDefault* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-118">Valore predefinito per il parametro *Property* .</span><span class="sxs-lookup"><span data-stu-id="f2f5c-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f2f5c-119">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2f5c-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f5c-120">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="f2f5c-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f5c-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2f5c-121">Return value</span></span>

<span data-ttu-id="f2f5c-122">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-122">This method can return one of these values.</span></span>



| <span data-ttu-id="f2f5c-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f2f5c-123">Return code</span></span>                                                                                   | <span data-ttu-id="f2f5c-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2f5c-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f2f5c-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2f5c-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f2f5c-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f2f5c-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f2f5c-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f2f5c-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f2f5c-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2f5c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2f5c-129">Requirements</span></span>



| <span data-ttu-id="f2f5c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f5c-130">Requirement</span></span> | <span data-ttu-id="f2f5c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f2f5c-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f5c-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f2f5c-132">TAPI version</span></span><br/> | <span data-ttu-id="f2f5c-133">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f2f5c-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f2f5c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2f5c-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f2f5c-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f5c-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2f5c-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2f5c-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f2f5c-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2f5c-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f2f5c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f2f5c-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f2f5c-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2f5c-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f5c-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2f5c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f5c-141">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="f2f5c-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="f2f5c-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="f2f5c-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="f2f5c-143">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="f2f5c-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




