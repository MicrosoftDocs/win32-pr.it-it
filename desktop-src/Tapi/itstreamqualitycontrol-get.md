---
description: Il metodo Get recupera il valore di una determinata proprietà di qualità del flusso.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Metodo ITStreamQualityControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328594"
---
# <a name="itstreamqualitycontrolget-method"></a><span data-ttu-id="42612-103">Metodo ITStreamQualityControl:: Get</span><span class="sxs-lookup"><span data-stu-id="42612-103">ITStreamQualityControl::Get method</span></span>

<span data-ttu-id="42612-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42612-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="42612-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="42612-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="42612-106">Il metodo **Get** Recupera il valore di una determinata [**proprietà di qualità del flusso**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="42612-106">The **Get** method retrieves the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42612-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42612-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="42612-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42612-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42612-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="42612-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42612-110">Membro dell'enumerazione [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="42612-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="42612-111">*plValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42612-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42612-112">Valore della *Proprietà* di input.</span><span class="sxs-lookup"><span data-stu-id="42612-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="42612-113">*plFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42612-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42612-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="42612-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42612-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42612-115">Return value</span></span>

<span data-ttu-id="42612-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="42612-116">This method can return one of these values.</span></span>



| <span data-ttu-id="42612-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="42612-117">Return code</span></span>                                                                                   | <span data-ttu-id="42612-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42612-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="42612-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42612-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="42612-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="42612-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="42612-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="42612-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="42612-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="42612-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42612-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42612-123">Requirements</span></span>



| <span data-ttu-id="42612-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="42612-124">Requirement</span></span> | <span data-ttu-id="42612-125">Valore</span><span class="sxs-lookup"><span data-stu-id="42612-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42612-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="42612-126">TAPI version</span></span><br/> | <span data-ttu-id="42612-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="42612-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="42612-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42612-128">Header</span></span><br/>       | <dl> <span data-ttu-id="42612-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42612-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42612-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="42612-130">Library</span></span><br/>      | <dl> <span data-ttu-id="42612-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42612-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="42612-132">DLL</span><span class="sxs-lookup"><span data-stu-id="42612-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="42612-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42612-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42612-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42612-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42612-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="42612-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="42612-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="42612-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="42612-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="42612-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




