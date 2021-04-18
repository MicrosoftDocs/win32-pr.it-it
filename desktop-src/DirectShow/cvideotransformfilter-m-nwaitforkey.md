---
description: Numero massimo corrente di fotogrammi Delta da eliminare.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324418"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="8c994-103">Membro nWaitForKey di CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="8c994-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="8c994-104">Numero massimo corrente di fotogrammi Delta da eliminare.</span><span class="sxs-lookup"><span data-stu-id="8c994-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="8c994-105">Sebbene la variabile sia maggiore di zero, il filtro ridurrà i frame fino a raggiungere un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="8c994-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="8c994-106">Per ogni frame eliminato, il filtro decrementa la variabile di uno, impedendo al filtro di eliminare un numero eccessivo di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="8c994-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="8c994-107">Dopo 30 frame Delta in una riga senza fotogrammi chiave, il filtro inizierà a recapito i frame.</span><span class="sxs-lookup"><span data-stu-id="8c994-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c994-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c994-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="8c994-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c994-109">Requirements</span></span>



| <span data-ttu-id="8c994-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c994-110">Requirement</span></span> | <span data-ttu-id="8c994-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8c994-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c994-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c994-112">Header</span></span><br/>  | <dl> <span data-ttu-id="8c994-113"><dt>Vtrans. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c994-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8c994-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c994-114">Library</span></span><br/> | <dl> <span data-ttu-id="8c994-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c994-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c994-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c994-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c994-117">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8c994-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




