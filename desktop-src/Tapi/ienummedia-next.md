---
description: Il metodo successivo ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Metodo IEnumMedia:: Next (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333148"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="63032-103">IEnumMedia:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="63032-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="63032-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63032-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="63032-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="63032-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="63032-106">Il metodo **successivo** ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="63032-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="63032-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63032-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="63032-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="63032-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63032-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63032-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63032-110">Numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="63032-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="63032-111">*pval* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="63032-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63032-112">Puntatore all'interfaccia [**ITmedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="63032-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="63032-113">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="63032-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63032-114">Puntatore al numero di elementi effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="63032-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="63032-115">Può essere **null** se *celt* è uno.</span><span class="sxs-lookup"><span data-stu-id="63032-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63032-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63032-116">Return value</span></span>

<span data-ttu-id="63032-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="63032-117">This method can return one of these values.</span></span>



| <span data-ttu-id="63032-118">Valore</span><span class="sxs-lookup"><span data-stu-id="63032-118">Value</span></span>                                                                                     | <span data-ttu-id="63032-119">Significato</span><span class="sxs-lookup"><span data-stu-id="63032-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="63032-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63032-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="63032-121">Il metodo ha restituito il numero *celt* di elementi.</span><span class="sxs-lookup"><span data-stu-id="63032-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="63032-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="63032-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="63032-123">Il numero di elementi rimanenti è minore di *celt*.</span><span class="sxs-lookup"><span data-stu-id="63032-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="63032-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="63032-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="63032-125">Il parametro *pval* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="63032-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="63032-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="63032-126">Remarks</span></span>

<span data-ttu-id="63032-127">TAPI chiama il metodo **AddRef** sull'interfaccia [**ITmedia**](itmedia.md) restituita da **IEnumMedia:: Next**.</span><span class="sxs-lookup"><span data-stu-id="63032-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="63032-128">L'applicazione deve chiamare **Release** sull'interfaccia **ITmedia** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="63032-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="63032-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63032-129">Requirements</span></span>



| <span data-ttu-id="63032-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="63032-130">Requirement</span></span> | <span data-ttu-id="63032-131">Valore</span><span class="sxs-lookup"><span data-stu-id="63032-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63032-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="63032-132">TAPI version</span></span><br/> | <span data-ttu-id="63032-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="63032-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="63032-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63032-134">Header</span></span><br/>       | <dl> <span data-ttu-id="63032-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="63032-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="63032-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="63032-136">Library</span></span><br/>      | <dl> <span data-ttu-id="63032-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63032-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="63032-138">DLL</span><span class="sxs-lookup"><span data-stu-id="63032-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="63032-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63032-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63032-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63032-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63032-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="63032-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




