---
description: "Flag per l'override dell'elaborazione batch. Se si imposta questo flag su TRUE, viene eseguito l'override del flag bBatchExact COutputQueue:: m e vengono recapitati \\_ tutti gli esempi in sospeso."
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'Membro COutputQueue:: m_bSendAnyway (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325752"
---
# <a name="coutputqueuem_bsendanyway-member"></a><span data-ttu-id="edddd-104">Membro bSendAnyway di COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="edddd-104">COutputQueue::m\_bSendAnyway member</span></span>

<span data-ttu-id="edddd-105">Flag per l'override dell'elaborazione batch.</span><span class="sxs-lookup"><span data-stu-id="edddd-105">Flag to override batch processing.</span></span> <span data-ttu-id="edddd-106">Se si imposta questo flag su **true** , viene eseguito l'override del flag [**\_ bBatchExact COutputQueue:: m**](coutputqueue-m-bbatchexact.md) e vengono recapitati tutti gli esempi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="edddd-106">Setting this flag to **TRUE** overrides the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) flag and delivers all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="edddd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edddd-107">Syntax</span></span>


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a><span data-ttu-id="edddd-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edddd-108">Requirements</span></span>



| <span data-ttu-id="edddd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="edddd-109">Requirement</span></span> | <span data-ttu-id="edddd-110">Valore</span><span class="sxs-lookup"><span data-stu-id="edddd-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edddd-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edddd-111">Header</span></span><br/>  | <dl> <span data-ttu-id="edddd-112"><dt>Outputq. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edddd-112"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="edddd-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="edddd-113">Library</span></span><br/> | <dl> <span data-ttu-id="edddd-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="edddd-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edddd-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edddd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edddd-116">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="edddd-116">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




