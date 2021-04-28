---
description: 'Metodo IEnumMedia::Next: il metodo Next ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: Metodo IEnumMedia::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113439"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="1b425-103">Metodo IEnumMedia::Next</span><span class="sxs-lookup"><span data-stu-id="1b425-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="1b425-104">\[ I controlli e le interfacce rendezvous IP Telephony Conferencing non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1b425-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b425-105">L'API client RTC offre funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="1b425-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1b425-106">Il **metodo Next** ottiene il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1b425-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b425-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b425-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="1b425-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b425-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b425-109">*celt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1b425-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b425-110">Numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="1b425-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="1b425-111">*pVal* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1b425-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b425-112">Puntatore [**all'interfaccia ITMedia.**](itmedia.md)</span><span class="sxs-lookup"><span data-stu-id="1b425-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1b425-113">*pceltFetched* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1b425-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b425-114">Puntatore al numero di elementi effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="1b425-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="1b425-115">Può essere **NULL se** *celt* è uno.</span><span class="sxs-lookup"><span data-stu-id="1b425-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b425-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b425-116">Return value</span></span>

<span data-ttu-id="1b425-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1b425-117">This method can return one of these values.</span></span>



| <span data-ttu-id="1b425-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1b425-118">Value</span></span>                                                                                     | <span data-ttu-id="1b425-119">Significato</span><span class="sxs-lookup"><span data-stu-id="1b425-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="1b425-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="1b425-121">Il metodo ha restituito il numero di elementi *celt.*</span><span class="sxs-lookup"><span data-stu-id="1b425-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="1b425-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="1b425-123">Il numero di elementi rimanenti è minore di *celt*.</span><span class="sxs-lookup"><span data-stu-id="1b425-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="1b425-124"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="1b425-125">Il *parametro pVal* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="1b425-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="1b425-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b425-126">Remarks</span></span>

<span data-ttu-id="1b425-127">TAPI chiama il **metodo AddRef** sull'interfaccia [**ITMedia**](itmedia.md) restituita da **IEnumMedia::Next.**</span><span class="sxs-lookup"><span data-stu-id="1b425-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="1b425-128">L'applicazione deve **chiamare Release** **sull'interfaccia ITMedia** per liberare le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="1b425-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b425-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b425-129">Requirements</span></span>



| <span data-ttu-id="1b425-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b425-130">Requirement</span></span> | <span data-ttu-id="1b425-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1b425-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b425-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="1b425-132">TAPI version</span></span><br/> | <span data-ttu-id="1b425-133">Richiede TAPI 3.0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1b425-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1b425-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b425-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1b425-135"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b425-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="1b425-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1b425-137"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1b425-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1b425-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1b425-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b425-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b425-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b425-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b425-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="1b425-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




