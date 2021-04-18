---
description: Legge i dati del filtro dal flusso specificato.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Metodo CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328926"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="28a12-103">CPersistStream. ReadFromStream, metodo</span><span class="sxs-lookup"><span data-stu-id="28a12-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="28a12-104">Legge i dati del filtro dal flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="28a12-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a12-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28a12-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="28a12-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28a12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a12-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="28a12-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="28a12-108">Puntatore a un'interfaccia **IStream** da cui leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="28a12-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a12-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28a12-109">Return value</span></span>

<span data-ttu-id="28a12-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="28a12-110">Returns S\_OK.</span></span> <span data-ttu-id="28a12-111">La classe derivata deve restituire un valore **HRESULT** valido.</span><span class="sxs-lookup"><span data-stu-id="28a12-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a12-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="28a12-112">Remarks</span></span>

<span data-ttu-id="28a12-113">La versione predefinita non legge nulla; è possibile eseguirne l'override per leggere i dati specifici della classe.</span><span class="sxs-lookup"><span data-stu-id="28a12-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a12-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28a12-114">Requirements</span></span>



| <span data-ttu-id="28a12-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28a12-115">Requirement</span></span> | <span data-ttu-id="28a12-116">Valore</span><span class="sxs-lookup"><span data-stu-id="28a12-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a12-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28a12-117">Header</span></span><br/>  | <dl> <span data-ttu-id="28a12-118"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28a12-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28a12-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="28a12-119">Library</span></span><br/> | <dl> <span data-ttu-id="28a12-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="28a12-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28a12-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28a12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a12-122">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="28a12-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




