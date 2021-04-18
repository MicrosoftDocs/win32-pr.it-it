---
description: 'Il metodo Skip ignora un numero specificato di tipi di supporti. Questo metodo implementa il metodo IEnumMediaTypes:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Metodo CEnumMediaTypes. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329849"
---
# <a name="cenummediatypesskip-method"></a><span data-ttu-id="8bf03-104">Metodo CEnumMediaTypes. Skip</span><span class="sxs-lookup"><span data-stu-id="8bf03-104">CEnumMediaTypes.Skip method</span></span>

<span data-ttu-id="8bf03-105">Il `Skip` metodo ignora un numero specificato di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="8bf03-105">The `Skip` method skips over a specified number of media types.</span></span> <span data-ttu-id="8bf03-106">Questo metodo implementa il metodo [**IEnumMediaTypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .</span><span class="sxs-lookup"><span data-stu-id="8bf03-106">This method implements the [**IEnumMediaTypes::Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf03-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bf03-107">Syntax</span></span>


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="8bf03-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bf03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf03-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="8bf03-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf03-110">Numero di tipi di supporto da ignorare.</span><span class="sxs-lookup"><span data-stu-id="8bf03-110">Number of media types to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf03-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bf03-111">Return value</span></span>

<span data-ttu-id="8bf03-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8bf03-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8bf03-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8bf03-113">Return code</span></span>                                                                                                | <span data-ttu-id="8bf03-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bf03-114">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf03-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-115"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="8bf03-116">Ignorato oltre la fine della sequenza.</span><span class="sxs-lookup"><span data-stu-id="8bf03-116">Skipped past the end of the sequence.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8bf03-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8bf03-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8bf03-118">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="8bf03-119"><dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-119"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="8bf03-120">Lo stato del PIN è stato modificato ed è ora incoerente con l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="8bf03-120">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bf03-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bf03-121">Requirements</span></span>



| <span data-ttu-id="8bf03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf03-122">Requirement</span></span> | <span data-ttu-id="8bf03-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8bf03-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf03-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bf03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8bf03-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8bf03-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bf03-126">Library</span></span><br/> | <dl> <span data-ttu-id="8bf03-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf03-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bf03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf03-129">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="8bf03-129">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




