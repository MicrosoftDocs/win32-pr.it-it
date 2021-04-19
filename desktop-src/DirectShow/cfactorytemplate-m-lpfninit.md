---
description: Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL. Può essere NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Membro CFactoryTemplate:: m_lpfnInit (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329820"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="83203-104">Membro lpfnInit di CFactoryTemplate:: m \_</span><span class="sxs-lookup"><span data-stu-id="83203-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="83203-105">Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="83203-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="83203-106">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="83203-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="83203-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83203-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="83203-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="83203-108">Remarks</span></span>

<span data-ttu-id="83203-109">Il tipo di puntatore a funzione è [**LPFNInitRoutine**](lpfninitroutine.md).</span><span class="sxs-lookup"><span data-stu-id="83203-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="83203-110">Se si specifica questa funzione nella DLL, la funzione del punto di ingresso della DLL la chiama con i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="83203-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="83203-111">*bLoading*: **true** quando la dll viene caricata, **false** quando la dll viene scaricata.</span><span class="sxs-lookup"><span data-stu-id="83203-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="83203-112">*rclsid*: puntatore al CLISD dell'oggetto, specificato nella variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="83203-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="83203-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83203-113">Requirements</span></span>



| <span data-ttu-id="83203-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="83203-114">Requirement</span></span> | <span data-ttu-id="83203-115">Valore</span><span class="sxs-lookup"><span data-stu-id="83203-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83203-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83203-116">Header</span></span><br/>  | <dl> <span data-ttu-id="83203-117"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83203-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83203-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="83203-118">Library</span></span><br/> | <dl> <span data-ttu-id="83203-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="83203-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83203-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83203-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83203-121">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="83203-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




