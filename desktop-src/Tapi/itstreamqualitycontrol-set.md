---
description: Il metodo set imposta il valore di una proprietà di qualità del flusso specificata.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Metodo ITStreamQualityControl:: set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328591"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="5a4b3-103">Metodo ITStreamQualityControl:: set</span><span class="sxs-lookup"><span data-stu-id="5a4b3-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="5a4b3-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a4b3-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5a4b3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a4b3-106">Il metodo **set** imposta il valore di una [**proprietà di qualità del flusso**](streamqualityproperty.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4b3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a4b3-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5a4b3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a4b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a4b3-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5a4b3-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4b3-110">Membro dell'enumerazione [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="5a4b3-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="5a4b3-111">*lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a4b3-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4b3-112">Valore desiderato per la *Proprietà* di input.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="5a4b3-113">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a4b3-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4b3-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="5a4b3-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a4b3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a4b3-115">Return value</span></span>

<span data-ttu-id="5a4b3-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-116">This method can return one of these values.</span></span>



| <span data-ttu-id="5a4b3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5a4b3-117">Value</span></span>                                                                                         | <span data-ttu-id="5a4b3-118">Significato</span><span class="sxs-lookup"><span data-stu-id="5a4b3-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5a4b3-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b3-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5a4b3-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5a4b3-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5a4b3-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5a4b3-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a4b3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a4b3-123">Requirements</span></span>



| <span data-ttu-id="5a4b3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a4b3-124">Requirement</span></span> | <span data-ttu-id="5a4b3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5a4b3-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4b3-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5a4b3-126">TAPI version</span></span><br/> | <span data-ttu-id="5a4b3-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="5a4b3-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="5a4b3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a4b3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="5a4b3-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b3-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a4b3-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a4b3-130">Library</span></span><br/>      | <dl> <span data-ttu-id="5a4b3-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b3-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5a4b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a4b3-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="5a4b3-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a4b3-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a4b3-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a4b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4b3-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="5a4b3-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="5a4b3-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="5a4b3-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="5a4b3-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="5a4b3-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




