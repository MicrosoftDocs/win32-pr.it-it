---
description: Sezione critica che protegge lo stato del flusso. Per ulteriori informazioni, vedere flusso di dati per gli sviluppatori di filtri.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Membro CTransformFilter:: m_csReceive (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331140"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="0c254-104">Membro csReceive di CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="0c254-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="0c254-105">Sezione critica che protegge lo stato del flusso.</span><span class="sxs-lookup"><span data-stu-id="0c254-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="0c254-106">Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0c254-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c254-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c254-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="0c254-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c254-108">Requirements</span></span>



| <span data-ttu-id="0c254-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c254-109">Requirement</span></span> | <span data-ttu-id="0c254-110">Valore</span><span class="sxs-lookup"><span data-stu-id="0c254-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c254-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c254-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0c254-112"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c254-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0c254-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c254-113">Library</span></span><br/> | <dl> <span data-ttu-id="0c254-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0c254-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c254-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c254-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c254-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="0c254-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




