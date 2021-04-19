---
description: Il metodo GetStreamCaps recupera le funzionalità associate a un indice di formato specificato.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Metodo ITFormatControl:: GetStreamCaps (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329456"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="cb7bb-103">Metodo ITFormatControl:: GetStreamCaps</span><span class="sxs-lookup"><span data-stu-id="cb7bb-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="cb7bb-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cb7bb-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cb7bb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cb7bb-106">Il metodo **GetStreamCaps** recupera le funzionalità associate a un indice di formato specificato.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb7bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb7bb-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cb7bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb7bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7bb-109">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cb7bb-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7bb-110">Indice del formato di cui viene eseguito il probe.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="cb7bb-111">*ppMediaType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb7bb-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7bb-112">Puntatore a un descrittore del **\_ \_ tipo di supporto am** del formato terminale.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="cb7bb-113">Per ulteriori informazioni sul **\_ \_ tipo di supporto am**, vedere la documentazione di DirectX.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="cb7bb-114">*pStreamConfigCaps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb7bb-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7bb-115">Struttura [**di \_ \_ \_ Caps di configurazione del flusso TAPI**](tapi-stream-config-caps.md) che fornisce informazioni dettagliate sulle funzionalità di flusso.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="cb7bb-116">*pfEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb7bb-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7bb-117">Indica se il formato associato all'indice corrente è abilitato.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7bb-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb7bb-118">Return value</span></span>

<span data-ttu-id="cb7bb-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-119">This method can return one of these values.</span></span>



| <span data-ttu-id="cb7bb-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cb7bb-120">Return code</span></span>                                                                                   | <span data-ttu-id="cb7bb-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb7bb-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cb7bb-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7bb-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cb7bb-123">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cb7bb-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7bb-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cb7bb-125">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb7bb-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb7bb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb7bb-126">Requirements</span></span>



| <span data-ttu-id="cb7bb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb7bb-127">Requirement</span></span> | <span data-ttu-id="cb7bb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cb7bb-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7bb-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="cb7bb-129">TAPI version</span></span><br/> | <span data-ttu-id="cb7bb-130">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="cb7bb-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="cb7bb-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb7bb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="cb7bb-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb7bb-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb7bb-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb7bb-133">Library</span></span><br/>      | <dl> <span data-ttu-id="cb7bb-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb7bb-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="cb7bb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cb7bb-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="cb7bb-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb7bb-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7bb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb7bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7bb-138">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="cb7bb-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="cb7bb-139">**\_ \_ tappi configurazione flusso TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="cb7bb-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




