---
description: 'Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive alla funzione membro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Metodo CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332336"
---
# <a name="cmediaeventgetidsofnames-method"></a><span data-ttu-id="43928-103">CMediaEvent. GetIDsOfNames, metodo</span><span class="sxs-lookup"><span data-stu-id="43928-103">CMediaEvent.GetIDsOfNames method</span></span>

<span data-ttu-id="43928-104">Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi, che possono essere usati durante le chiamate successive alla funzione membro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="43928-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used upon subsequent calls to the [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="43928-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43928-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="43928-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43928-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="43928-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="43928-108">Identificatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="43928-108">Reference identifier.</span></span> <span data-ttu-id="43928-109">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="43928-109">Reserved for future use.</span></span> <span data-ttu-id="43928-110">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="43928-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43928-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="43928-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="43928-112">Indirizzo di un puntatore a una matrice di nomi passata di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="43928-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="43928-113">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="43928-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="43928-114">Conteggio dei nomi di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="43928-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="43928-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="43928-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="43928-116">Contesto delle impostazioni locali in cui interpretare i nomi.</span><span class="sxs-lookup"><span data-stu-id="43928-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="43928-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="43928-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="43928-118">Puntatore a una matrice allocata dal chiamante, ogni elemento contenente un ID corrispondente a uno dei nomi passati nella matrice *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="43928-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="43928-119">Il primo elemento rappresenta il nome del membro; gli elementi successivi rappresentano ognuno dei parametri del membro.</span><span class="sxs-lookup"><span data-stu-id="43928-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43928-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43928-120">Return value</span></span>

<span data-ttu-id="43928-121">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="43928-121">Returns one of the following values.</span></span>



| <span data-ttu-id="43928-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="43928-122">Return code</span></span>                                                                                            | <span data-ttu-id="43928-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43928-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43928-124"><dt>**\_ \_ CLSID sconosciuto disp \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="43928-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="43928-125">Il CLSID non è stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="43928-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="43928-126"><dt>**DISP \_ E \_ unknowname**</dt></span><span class="sxs-lookup"><span data-stu-id="43928-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="43928-127">Uno o più nomi non sono noti.</span><span class="sxs-lookup"><span data-stu-id="43928-127">One or more of the names were not known.</span></span> <span data-ttu-id="43928-128">I DISPID restituiti contengono DISPID \_ sconosciuto per ogni voce che corrisponde a un nome sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="43928-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="43928-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="43928-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="43928-130">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="43928-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="43928-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="43928-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="43928-132">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="43928-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="43928-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43928-133">Requirements</span></span>



| <span data-ttu-id="43928-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="43928-134">Requirement</span></span> | <span data-ttu-id="43928-135">Valore</span><span class="sxs-lookup"><span data-stu-id="43928-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43928-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43928-136">Header</span></span><br/>  | <dl> <span data-ttu-id="43928-137"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43928-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43928-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="43928-138">Library</span></span><br/> | <dl> <span data-ttu-id="43928-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43928-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43928-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43928-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43928-141">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="43928-141">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




