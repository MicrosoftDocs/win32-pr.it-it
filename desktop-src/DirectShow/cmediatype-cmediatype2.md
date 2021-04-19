---
description: Informazioni sul metodo del costruttore CMediaType. CMediaType (mtype. h). Questo metodo usa il parametro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Costruttore CMediaType. CMediaType (mtype. h)-parametro majortype
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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323832"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="e3b06-104">Costruttore CMediaType. CMediaType (mtype. h)-parametro majortype</span><span class="sxs-lookup"><span data-stu-id="e3b06-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="e3b06-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e3b06-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b06-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3b06-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="e3b06-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3b06-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b06-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="e3b06-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="e3b06-109">Puntatore a un **GUID** di tipo principale.</span><span class="sxs-lookup"><span data-stu-id="e3b06-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="e3b06-110">Il costruttore inizializza il GUID del tipo principale su questo valore.</span><span class="sxs-lookup"><span data-stu-id="e3b06-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3b06-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3b06-111">Remarks</span></span>

<span data-ttu-id="e3b06-112">Il costruttore chiama il metodo [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e3b06-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b06-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3b06-113">Requirements</span></span>

| <span data-ttu-id="e3b06-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b06-114">Requirement</span></span>                   | <span data-ttu-id="e3b06-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b06-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b06-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3b06-116">Header</span></span>  | <span data-ttu-id="e3b06-117">Mtype. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="e3b06-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="e3b06-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e3b06-118">Library</span></span> | <span data-ttu-id="e3b06-119">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="e3b06-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e3b06-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3b06-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b06-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e3b06-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




