---
description: Il metodo ReOrderCapabilities imposta un nuovo ordine per le funzionalità di formattazione.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Metodo ITFormatControl:: ReOrderCapabilities (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329448"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="db6a2-103">Metodo ITFormatControl:: ReOrderCapabilities</span><span class="sxs-lookup"><span data-stu-id="db6a2-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="db6a2-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db6a2-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db6a2-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="db6a2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="db6a2-106">Il metodo **ReOrderCapabilities** imposta un nuovo ordine per le funzionalità di formattazione.</span><span class="sxs-lookup"><span data-stu-id="db6a2-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db6a2-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="db6a2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db6a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6a2-109">*pdwIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6a2-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a2-110">Indice del formato riordinato.</span><span class="sxs-lookup"><span data-stu-id="db6a2-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="db6a2-111">*pfEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6a2-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a2-112">Indica se il formato deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="db6a2-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="db6a2-113">*pfPublicize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6a2-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a2-114">Indica se il formato deve essere reso disponibile.</span><span class="sxs-lookup"><span data-stu-id="db6a2-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="db6a2-115">*dwNumIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6a2-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6a2-116">Nuovo numero di indice per il formato.</span><span class="sxs-lookup"><span data-stu-id="db6a2-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6a2-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db6a2-117">Return value</span></span>

<span data-ttu-id="db6a2-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="db6a2-118">This method can return one of these values.</span></span>



| <span data-ttu-id="db6a2-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="db6a2-119">Return code</span></span>                                                                                   | <span data-ttu-id="db6a2-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db6a2-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="db6a2-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db6a2-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="db6a2-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="db6a2-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="db6a2-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="db6a2-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="db6a2-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="db6a2-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db6a2-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="db6a2-125">Remarks</span></span>

<span data-ttu-id="db6a2-126">Il metodo [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) deve essere chiamato prima di usare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="db6a2-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6a2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db6a2-127">Requirements</span></span>



| <span data-ttu-id="db6a2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="db6a2-128">Requirement</span></span> | <span data-ttu-id="db6a2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="db6a2-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="db6a2-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="db6a2-130">TAPI version</span></span><br/> | <span data-ttu-id="db6a2-131">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="db6a2-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="db6a2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db6a2-132">Header</span></span><br/>       | <dl> <span data-ttu-id="db6a2-133"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6a2-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db6a2-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="db6a2-134">Library</span></span><br/>      | <dl> <span data-ttu-id="db6a2-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db6a2-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="db6a2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="db6a2-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="db6a2-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6a2-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db6a2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db6a2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6a2-139">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="db6a2-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="db6a2-140">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="db6a2-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




