---
description: Il metodo NotifyMediaType invia una notifica all'oggetto CDrawImage del tipo di supporto corrente.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Metodo CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331920"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="f3012-103">CDrawImage. NotifyMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="f3012-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="f3012-104">Il `NotifyMediaType` metodo notifica all'oggetto **CDrawImage** del tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="f3012-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3012-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3012-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="f3012-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3012-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="f3012-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="f3012-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) o **null** per cancellare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f3012-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3012-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3012-109">Return value</span></span>

<span data-ttu-id="f3012-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f3012-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3012-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3012-111">Remarks</span></span>

<span data-ttu-id="f3012-112">Il filtro proprietario deve chiamare questo metodo ogni volta che viene modificato il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="f3012-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="f3012-113">Questa situazione si verifica in genere quando il pin si connette per la prima volta e dopo una modifica del formato dinamico.</span><span class="sxs-lookup"><span data-stu-id="f3012-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="f3012-114">L'oggetto **CDrawImage** archivia il puntatore *pMediaType* nella variabile **membro \_ pMediaType m** .</span><span class="sxs-lookup"><span data-stu-id="f3012-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="f3012-115">Se pertanto il chiamante deve rilasciare l'oggetto **CMediaType** , deve aggiornare l'oggetto **CDrawImage** chiamando nuovamente questo metodo con un nuovo puntatore o con un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="f3012-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="f3012-116">In caso contrario, può verificarsi un errore quando l'oggetto **CDrawImage** tenta di fare riferimento al puntatore precedente.</span><span class="sxs-lookup"><span data-stu-id="f3012-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3012-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3012-117">Requirements</span></span>



| <span data-ttu-id="f3012-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3012-118">Requirement</span></span> | <span data-ttu-id="f3012-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f3012-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3012-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3012-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f3012-121"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3012-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3012-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3012-122">Library</span></span><br/> | <dl> <span data-ttu-id="f3012-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3012-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3012-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3012-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3012-125">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="f3012-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




