---
description: Costruttore CMediaType.CMediaType (Mtype.h) - Metodo costruttore.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Costruttore CMediaType.CMediaType (Mtype.h): parametri cmtype e phr'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095419"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="181a0-103">Costruttore CMediaType.CMediaType (Mtype.h)</span><span class="sxs-lookup"><span data-stu-id="181a0-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="181a0-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="181a0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="181a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="181a0-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="181a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="181a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="181a0-107">*cmtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="181a0-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="181a0-108">Riferimento a un `CMediaType` oggetto .</span><span class="sxs-lookup"><span data-stu-id="181a0-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="181a0-109">Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se presente.</span><span class="sxs-lookup"><span data-stu-id="181a0-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="181a0-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="181a0-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="181a0-111">Puntatore a una variabile che riceve un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="181a0-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="181a0-112">Questo parametro può essere un **puntatore NULL.**</span><span class="sxs-lookup"><span data-stu-id="181a0-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="181a0-113">In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore.</span><span class="sxs-lookup"><span data-stu-id="181a0-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="181a0-114">Se il costruttore ha esito negativo, imposta il valore su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="181a0-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="181a0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="181a0-115">Remarks</span></span>

<span data-ttu-id="181a0-116">Il costruttore chiama il [**metodo CMediaType::InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="181a0-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="181a0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="181a0-117">Requirements</span></span>



| <span data-ttu-id="181a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="181a0-118">Requirement</span></span> | <span data-ttu-id="181a0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="181a0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181a0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="181a0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="181a0-121"><dt>Mtype.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="181a0-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="181a0-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="181a0-122">Library</span></span><br/> | <dl> <span data-ttu-id="181a0-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="181a0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181a0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="181a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181a0-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="181a0-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




