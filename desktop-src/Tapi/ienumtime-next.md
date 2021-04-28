---
description: 'Metodo IEnumTime::Next: il metodo Next ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: Metodo IEnumTime::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118389"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="d75af-103">Metodo IEnumTime::Next</span><span class="sxs-lookup"><span data-stu-id="d75af-103">IEnumTime::Next method</span></span>

<span data-ttu-id="d75af-104">\[ Le interfacce e i controlli di conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d75af-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d75af-105">L'API client rtc offre funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="d75af-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d75af-106">Il **metodo Next** ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d75af-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75af-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d75af-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d75af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d75af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75af-109">*celt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d75af-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75af-110">Numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="d75af-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="d75af-111">*pVal* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d75af-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d75af-112">Puntatore [**all'interfaccia ITTime.**](ittime.md)</span><span class="sxs-lookup"><span data-stu-id="d75af-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d75af-113">*pceltFetched* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d75af-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d75af-114">Puntatore al numero di elementi effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="d75af-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="d75af-115">Può essere **NULL se** *celt* è 1.</span><span class="sxs-lookup"><span data-stu-id="d75af-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75af-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d75af-116">Return value</span></span>

<span data-ttu-id="d75af-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d75af-117">This method can return one of these values.</span></span>



| <span data-ttu-id="d75af-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d75af-118">Value</span></span>                                                                                     | <span data-ttu-id="d75af-119">Significato</span><span class="sxs-lookup"><span data-stu-id="d75af-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="d75af-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d75af-121">Il metodo ha restituito il numero di elementi *celt.*</span><span class="sxs-lookup"><span data-stu-id="d75af-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="d75af-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d75af-123">Il numero di elementi rimanenti è minore di *celt*.</span><span class="sxs-lookup"><span data-stu-id="d75af-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="d75af-124"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d75af-125">Il *parametro pVal* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="d75af-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="d75af-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d75af-126">Remarks</span></span>

<span data-ttu-id="d75af-127">TAPI chiama il **metodo AddRef** [**sull'interfaccia ITTime**](ittime.md) restituita da **IEnumTime::Next**.</span><span class="sxs-lookup"><span data-stu-id="d75af-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="d75af-128">L'applicazione deve **chiamare Release** **sull'interfaccia ITTime** per liberare le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="d75af-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75af-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d75af-129">Requirements</span></span>



| <span data-ttu-id="d75af-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75af-130">Requirement</span></span> | <span data-ttu-id="d75af-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d75af-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d75af-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d75af-132">TAPI version</span></span><br/> | <span data-ttu-id="d75af-133">Richiede TAPI 3.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d75af-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d75af-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d75af-134">Header</span></span><br/>       | <dl> <span data-ttu-id="d75af-135"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d75af-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="d75af-136">Library</span></span><br/>      | <dl> <span data-ttu-id="d75af-137"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d75af-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d75af-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="d75af-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75af-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75af-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d75af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75af-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="d75af-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




