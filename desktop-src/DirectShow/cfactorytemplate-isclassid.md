---
description: Il metodo IsClassID determina se un CLSID corrisponde a questo modello di classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Metodo CFactoryTemplate. IsClassID (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329830"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="96ef7-103">CFactoryTemplate. IsClassID, metodo</span><span class="sxs-lookup"><span data-stu-id="96ef7-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="96ef7-104">Il `IsClassID` metodo determina se un CLSID corrisponde a questo modello di classe.</span><span class="sxs-lookup"><span data-stu-id="96ef7-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ef7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96ef7-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="96ef7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96ef7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96ef7-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="96ef7-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="96ef7-108">Riferimento a un CLSID.</span><span class="sxs-lookup"><span data-stu-id="96ef7-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96ef7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96ef7-109">Return value</span></span>

<span data-ttu-id="96ef7-110">Restituisce **true** se il *parametro rclsid* è lo stesso CLSID della variabile membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) . in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="96ef7-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="96ef7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96ef7-111">Requirements</span></span>



| <span data-ttu-id="96ef7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="96ef7-112">Requirement</span></span> | <span data-ttu-id="96ef7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="96ef7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ef7-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96ef7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="96ef7-115"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96ef7-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="96ef7-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="96ef7-116">Library</span></span><br/> | <dl> <span data-ttu-id="96ef7-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="96ef7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96ef7-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96ef7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96ef7-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="96ef7-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




