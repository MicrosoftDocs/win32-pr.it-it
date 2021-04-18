---
description: Scrive i dati del filtro nel flusso specificato.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Metodo CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328915"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="f19d3-103">CPersistStream. WriteToStream, metodo</span><span class="sxs-lookup"><span data-stu-id="f19d3-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="f19d3-104">Scrive i dati del filtro nel flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="f19d3-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f19d3-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="f19d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f19d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19d3-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="f19d3-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="f19d3-108">Puntatore a un'interfaccia **IStream** che specifica il flusso di destinazione dei dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="f19d3-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19d3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f19d3-109">Return value</span></span>

<span data-ttu-id="f19d3-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f19d3-110">Returns S\_OK.</span></span> <span data-ttu-id="f19d3-111">La classe derivata deve restituire un valore **HRESULT** valido.</span><span class="sxs-lookup"><span data-stu-id="f19d3-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19d3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f19d3-112">Remarks</span></span>

<span data-ttu-id="f19d3-113">La versione predefinita non scrive nulla; è possibile eseguirne l'override per scrivere i dati specifici della classe.</span><span class="sxs-lookup"><span data-stu-id="f19d3-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19d3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f19d3-114">Requirements</span></span>



| <span data-ttu-id="f19d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19d3-115">Requirement</span></span> | <span data-ttu-id="f19d3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f19d3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19d3-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f19d3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f19d3-118"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f19d3-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f19d3-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f19d3-119">Library</span></span><br/> | <dl> <span data-ttu-id="f19d3-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f19d3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f19d3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f19d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19d3-122">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="f19d3-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




