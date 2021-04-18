---
description: Velocità di riproduzione. Per impostazione predefinita, il valore è impostato su 1,0.
ms.assetid: 835ddbe8-2017-4a4a-8f10-b3f33a8215a7
title: 'Membro CSourceSeeking:: m_dRateSeeking (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dRateSeeking
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1055a420316868db6374798c0295339dd74ac172
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329495"
---
# <a name="csourceseekingm_drateseeking-member"></a><span data-ttu-id="0d710-104">Membro dRateSeeking di CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="0d710-104">CSourceSeeking::m\_dRateSeeking member</span></span>

<span data-ttu-id="0d710-105">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0d710-105">Playback rate.</span></span> <span data-ttu-id="0d710-106">Per impostazione predefinita, il valore è impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="0d710-106">By default, the value is set to 1.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d710-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d710-107">Syntax</span></span>


```C++
double m_dRateSeeking;
```



## <a name="remarks"></a><span data-ttu-id="0d710-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="0d710-108">Remarks</span></span>

<span data-ttu-id="0d710-109">Prima di accedere a questa variabile, mantenere la sezione **\_ pLock critico m** .</span><span class="sxs-lookup"><span data-stu-id="0d710-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d710-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d710-110">Requirements</span></span>



| <span data-ttu-id="0d710-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d710-111">Requirement</span></span> | <span data-ttu-id="0d710-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0d710-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d710-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d710-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0d710-114"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d710-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0d710-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d710-115">Library</span></span><br/> | <dl> <span data-ttu-id="0d710-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d710-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d710-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d710-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d710-118">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="0d710-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




