---
description: Blocco per proteggere la creazione di oggetti all'interno del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332212"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="52854-103">Membro ObjectCreationLock di CBaseRenderer:: m \_</span><span class="sxs-lookup"><span data-stu-id="52854-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="52854-104">Blocco per proteggere la creazione di oggetti all'interno del filtro.</span><span class="sxs-lookup"><span data-stu-id="52854-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="52854-105">Il filtro utilizza questo blocco quando crea il pin di input ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o l'oggetto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)).</span><span class="sxs-lookup"><span data-stu-id="52854-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="52854-106">Questo blocco impedisce a più thread di tentare di creare uno di questi oggetti nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="52854-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="52854-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52854-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="52854-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52854-108">Requirements</span></span>



| <span data-ttu-id="52854-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="52854-109">Requirement</span></span> | <span data-ttu-id="52854-110">Valore</span><span class="sxs-lookup"><span data-stu-id="52854-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52854-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52854-111">Header</span></span><br/>  | <dl> <span data-ttu-id="52854-112"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52854-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="52854-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="52854-113">Library</span></span><br/> | <dl> <span data-ttu-id="52854-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="52854-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52854-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52854-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52854-116">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="52854-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




