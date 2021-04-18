---
description: Nome del PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membro CBasePin:: m_pName (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331523"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="3ab9d-103">Membro pName di CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="3ab9d-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="3ab9d-104">Nome del PIN.</span><span class="sxs-lookup"><span data-stu-id="3ab9d-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab9d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ab9d-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="3ab9d-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3ab9d-106">Remarks</span></span>

<span data-ttu-id="3ab9d-107">Il metodo [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) restituisce questa stringa come nome del PIN e il metodo [**CBasePin:: QueryId**](cbasepin-queryid.md) lo restituisce come identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="3ab9d-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="3ab9d-108">In generale, tuttavia, il nome del PIN e l'identificatore del PIN non devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="3ab9d-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="3ab9d-109">L'identificatore del PIN viene usato per la persistenza del grafo.</span><span class="sxs-lookup"><span data-stu-id="3ab9d-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="3ab9d-110">Per ulteriori informazioni, vedere [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="3ab9d-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab9d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ab9d-111">Requirements</span></span>



| <span data-ttu-id="3ab9d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab9d-112">Requirement</span></span> | <span data-ttu-id="3ab9d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3ab9d-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab9d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ab9d-114">Header</span></span><br/> | <dl> <span data-ttu-id="3ab9d-115"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ab9d-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ab9d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ab9d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab9d-117">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="3ab9d-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




