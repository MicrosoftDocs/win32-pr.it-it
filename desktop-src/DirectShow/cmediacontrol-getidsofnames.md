---
description: 'Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi (DISPID), che possono essere usati durante le chiamate successive alla funzione membro CMediaControl:: Invoke.'
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: Metodo CMediaControl. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f906db9540f0429e1e7831284e55edf8c29b6a03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328347"
---
# <a name="cmediacontrolgetidsofnames-method"></a><span data-ttu-id="786e0-103">CMediaControl. GetIDsOfNames, metodo</span><span class="sxs-lookup"><span data-stu-id="786e0-103">CMediaControl.GetIDsOfNames method</span></span>

<span data-ttu-id="786e0-104">Esegue il mapping di una singola funzione membro e di un set facoltativo di parametri a un set corrispondente di identificatori di invio di numeri interi (DISPID), che possono essere usati durante le chiamate successive alla funzione membro [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="786e0-104">Maps a single member function and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used upon subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="786e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="786e0-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="786e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="786e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="786e0-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="786e0-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="786e0-108">Identificatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="786e0-108">Reference identifier.</span></span> <span data-ttu-id="786e0-109">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="786e0-109">Reserved for future use.</span></span> <span data-ttu-id="786e0-110">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="786e0-110">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="786e0-111">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="786e0-111">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="786e0-112">Indirizzo di un puntatore a una matrice di nomi passata di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="786e0-112">Address of a pointer to a passed-in array of names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="786e0-113">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="786e0-113">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="786e0-114">Conteggio dei nomi di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="786e0-114">Count of the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="786e0-115">*lcid*</span><span class="sxs-lookup"><span data-stu-id="786e0-115">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="786e0-116">Contesto delle impostazioni locali in cui interpretare i nomi.</span><span class="sxs-lookup"><span data-stu-id="786e0-116">Locale context in which to interpret the names.</span></span>

</dd> <dt>

<span data-ttu-id="786e0-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="786e0-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="786e0-118">Puntatore a una matrice allocata dal chiamante, ogni elemento contenente un ID corrispondente a uno dei nomi passati nella matrice *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="786e0-118">Pointer to a caller-allocated array, each element of which contains an ID corresponding to one of the names passed in the *rgszNames* array.</span></span> <span data-ttu-id="786e0-119">Il primo elemento rappresenta il nome del membro; gli elementi successivi rappresentano ognuno dei parametri del membro.</span><span class="sxs-lookup"><span data-stu-id="786e0-119">The first element represents the member name; the subsequent elements represent each of the member's parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="786e0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="786e0-120">Return value</span></span>

<span data-ttu-id="786e0-121">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="786e0-121">Returns one of the following values.</span></span>



| <span data-ttu-id="786e0-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="786e0-122">Return code</span></span>                                                                                            | <span data-ttu-id="786e0-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="786e0-123">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="786e0-124"><dt>**\_ \_ CLSID sconosciuto disp \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-124"><dt>**DISP\_E\_UNKNOWN\_CLSID**</dt></span></span> </dl> | <span data-ttu-id="786e0-125">Il CLSID non è stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="786e0-125">The CLSID was not recognized.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="786e0-126"><dt>**DISP \_ E \_ unknowname**</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-126"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl>    | <span data-ttu-id="786e0-127">Uno o più nomi non sono noti.</span><span class="sxs-lookup"><span data-stu-id="786e0-127">One or more of the names were not known.</span></span> <span data-ttu-id="786e0-128">I DISPID restituiti contengono DISPID \_ sconosciuto per ogni voce che corrisponde a un nome sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="786e0-128">The returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span><br/> |
| <dl> <span data-ttu-id="786e0-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="786e0-130">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="786e0-130">Out of memory.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="786e0-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-131"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="786e0-132">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="786e0-132">Success.</span></span><br/>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="786e0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="786e0-133">Requirements</span></span>



| <span data-ttu-id="786e0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="786e0-134">Requirement</span></span> | <span data-ttu-id="786e0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="786e0-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="786e0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="786e0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="786e0-137"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="786e0-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="786e0-138">Library</span></span><br/> | <dl> <span data-ttu-id="786e0-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="786e0-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786e0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="786e0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786e0-141">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="786e0-141">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




