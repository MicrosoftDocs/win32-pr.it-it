---
description: Il \_ sottoflusso get ottiene un puntatore a una matrice di interfacce ITSubStream che rappresentano i flussi sottoflussi necessari nell'evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Metodo ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328730"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="009a8-103">Metodo ITParticipantEvent:: Get \_ substream</span><span class="sxs-lookup"><span data-stu-id="009a8-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="009a8-104">\[**ottenere \_ Il sottoflusso** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="009a8-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="009a8-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="009a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="009a8-106">Il **\_ sottoflusso Get** ottiene un puntatore a una matrice di interfacce [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) che rappresentano i flussi sottoflussi necessari nell'evento.</span><span class="sxs-lookup"><span data-stu-id="009a8-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="009a8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="009a8-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="009a8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="009a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009a8-109">*ppSubStream* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="009a8-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="009a8-110">Puntatore alla matrice di puntatori [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="009a8-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009a8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="009a8-111">Return value</span></span>

<span data-ttu-id="009a8-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="009a8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="009a8-113">Valore</span><span class="sxs-lookup"><span data-stu-id="009a8-113">Value</span></span>                                                                                           | <span data-ttu-id="009a8-114">Significato</span><span class="sxs-lookup"><span data-stu-id="009a8-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="009a8-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="009a8-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="009a8-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="009a8-117"><dt>**TAPI \_ E \_ noitems**</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="009a8-118">All'evento non è associato alcun flusso.</span><span class="sxs-lookup"><span data-stu-id="009a8-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="009a8-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="009a8-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="009a8-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="009a8-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="009a8-122">Il parametro *ppSubStream* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="009a8-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="009a8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="009a8-123">Requirements</span></span>



| <span data-ttu-id="009a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="009a8-124">Requirement</span></span> | <span data-ttu-id="009a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="009a8-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="009a8-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="009a8-126">TAPI version</span></span><br/> | <span data-ttu-id="009a8-127">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="009a8-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="009a8-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="009a8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="009a8-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="009a8-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="009a8-130">Library</span></span><br/>      | <dl> <span data-ttu-id="009a8-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="009a8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="009a8-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="009a8-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="009a8-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="009a8-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="009a8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009a8-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="009a8-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="009a8-136">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="009a8-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

