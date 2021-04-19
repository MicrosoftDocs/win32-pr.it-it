---
description: Recupera la dimensione massima in byte necessaria per il flusso corrente, senza includere il numero di versione.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Metodo CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328921"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="a847c-103">CPersistStream. SizeMax, metodo</span><span class="sxs-lookup"><span data-stu-id="a847c-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="a847c-104">Recupera la dimensione massima in byte necessaria per il flusso corrente, senza includere il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="a847c-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a847c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a847c-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="a847c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a847c-106">Parameters</span></span>

<span data-ttu-id="a847c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a847c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a847c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a847c-108">Return value</span></span>

<span data-ttu-id="a847c-109">Restituisce il numero di byte necessari per i dati, escluso il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="a847c-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="a847c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a847c-110">Remarks</span></span>

<span data-ttu-id="a847c-111">La versione predefinita restituisce zero. è necessario eseguirne l'override per fornire un altro valore appropriato.</span><span class="sxs-lookup"><span data-stu-id="a847c-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a847c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a847c-112">Requirements</span></span>



| <span data-ttu-id="a847c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a847c-113">Requirement</span></span> | <span data-ttu-id="a847c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a847c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a847c-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a847c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a847c-116"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a847c-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a847c-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="a847c-117">Library</span></span><br/> | <dl> <span data-ttu-id="a847c-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a847c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a847c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a847c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a847c-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="a847c-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




