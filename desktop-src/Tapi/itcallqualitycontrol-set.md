---
description: Il metodo set imposta il valore di una determinata proprietà del controllo di qualità della chiamata.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Metodo ITCallQualityControl:: set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328238"
---
# <a name="itcallqualitycontrolset-method"></a><span data-ttu-id="81046-103">Metodo ITCallQualityControl:: set</span><span class="sxs-lookup"><span data-stu-id="81046-103">ITCallQualityControl::Set method</span></span>

<span data-ttu-id="81046-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="81046-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="81046-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="81046-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="81046-106">Il metodo **set** imposta il valore di una determinata [proprietà del controllo di qualità della chiamata](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="81046-106">The **Set** method sets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81046-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81046-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="81046-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81046-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81046-109">*Proprietà* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="81046-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81046-110">Membro dell'enumerazione [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="81046-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="81046-111">*lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81046-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81046-112">Valore desiderato per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="81046-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="81046-113">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81046-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81046-114">Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .</span><span class="sxs-lookup"><span data-stu-id="81046-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81046-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81046-115">Return value</span></span>

<span data-ttu-id="81046-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="81046-116">This method can return one of these values.</span></span>



| <span data-ttu-id="81046-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="81046-117">Return code</span></span>                                                                                   | <span data-ttu-id="81046-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81046-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="81046-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="81046-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="81046-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="81046-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="81046-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="81046-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="81046-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="81046-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81046-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81046-123">Requirements</span></span>



| <span data-ttu-id="81046-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="81046-124">Requirement</span></span> | <span data-ttu-id="81046-125">Valore</span><span class="sxs-lookup"><span data-stu-id="81046-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81046-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="81046-126">TAPI version</span></span><br/> | <span data-ttu-id="81046-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="81046-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="81046-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81046-128">Header</span></span><br/>       | <dl> <span data-ttu-id="81046-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81046-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81046-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="81046-130">Library</span></span><br/>      | <dl> <span data-ttu-id="81046-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81046-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="81046-132">DLL</span><span class="sxs-lookup"><span data-stu-id="81046-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="81046-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81046-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81046-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81046-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81046-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="81046-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="81046-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="81046-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="81046-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="81046-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




