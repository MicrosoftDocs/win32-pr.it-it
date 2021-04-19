---
description: Il \_ metodo Get MediaTypes ottiene i tipi di supporto associati a un partecipante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Metodo ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324234"
---
# <a name="itparticipantget_mediatypes-method"></a><span data-ttu-id="5b6a6-103">Metodo ITParticipant:: Get \_ MediaTypes</span><span class="sxs-lookup"><span data-stu-id="5b6a6-103">ITParticipant::get\_MediaTypes method</span></span>

<span data-ttu-id="5b6a6-104">\[**ottenere \_ MediaTypes** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-104">\[**get\_MediaTypes** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5b6a6-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="5b6a6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5b6a6-106">Il metodo **get \_ MediaTypes** ottiene i [**tipi di supporto**](tapimediatype--constants.md) associati a un partecipante.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-106">The **get\_MediaTypes** method gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b6a6-107">Syntax</span></span>


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="5b6a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b6a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b6a6-109">*plMediaType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b6a6-109">*plMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b6a6-110">Puntatore ai flag del tipo di supporto, ad esempio \_ video TAPIMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-110">Pointer to media type flags, such as TAPIMEDIATYPE\_VIDEO.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b6a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b6a6-111">Return value</span></span>

<span data-ttu-id="5b6a6-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-112">This method can return one of these values.</span></span>



| <span data-ttu-id="5b6a6-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5b6a6-113">Return code</span></span>                                                                                   | <span data-ttu-id="5b6a6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b6a6-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5b6a6-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5b6a6-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5b6a6-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5b6a6-118">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-118">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5b6a6-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5b6a6-120">Il parametro *plMediaType* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="5b6a6-120">The *plMediaType* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="5b6a6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b6a6-121">Requirements</span></span>



| <span data-ttu-id="5b6a6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6a6-122">Requirement</span></span> | <span data-ttu-id="5b6a6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5b6a6-123">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6a6-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5b6a6-124">TAPI version</span></span><br/> | <span data-ttu-id="5b6a6-125">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5b6a6-125">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="5b6a6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b6a6-126">Header</span></span><br/>       | <dl> <span data-ttu-id="5b6a6-127"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-127"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b6a6-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b6a6-128">Library</span></span><br/>      | <dl> <span data-ttu-id="5b6a6-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-129"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5b6a6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5b6a6-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="5b6a6-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b6a6-131"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b6a6-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b6a6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b6a6-133">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="5b6a6-133">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="5b6a6-134">**tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="5b6a6-134">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

 




