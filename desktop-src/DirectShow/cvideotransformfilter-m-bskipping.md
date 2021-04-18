---
description: Valore booleano che indica se il filtro sta attualmente eliminando i frame. Se questo valore è TRUE, il filtro continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 frame Delta in una riga senza un fotogramma chiave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Membro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330194"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="cae97-104">Membro bSkipping di CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="cae97-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="cae97-105">Valore booleano che indica se il filtro sta attualmente eliminando i frame.</span><span class="sxs-lookup"><span data-stu-id="cae97-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="cae97-106">Se questo valore è **true**, il filtro continua a rilasciare i frame fino a raggiungere il fotogramma chiave successivo o fino a quando non riceve 30 frame Delta in una riga senza un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="cae97-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cae97-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="cae97-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cae97-108">Requirements</span></span>



| <span data-ttu-id="cae97-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae97-109">Requirement</span></span> | <span data-ttu-id="cae97-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cae97-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae97-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cae97-111">Header</span></span><br/>  | <dl> <span data-ttu-id="cae97-112"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cae97-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cae97-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="cae97-113">Library</span></span><br/> | <dl> <span data-ttu-id="cae97-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cae97-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae97-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cae97-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae97-116">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="cae97-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




