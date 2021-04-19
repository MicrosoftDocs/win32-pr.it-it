---
description: Il metodo IsUsingDefaultSource determina se il renderer utilizza la finestra di origine predefinita.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Metodo CBaseControlVideo. IsUsingDefaultSource (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333499"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="f2bf3-103">CBaseControlVideo. IsUsingDefaultSource, metodo</span><span class="sxs-lookup"><span data-stu-id="f2bf3-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="f2bf3-104">Il `IsUsingDefaultSource` metodo determina se il renderer utilizza la finestra di origine predefinita.</span><span class="sxs-lookup"><span data-stu-id="f2bf3-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bf3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2bf3-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="f2bf3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2bf3-106">Parameters</span></span>

<span data-ttu-id="f2bf3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f2bf3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2bf3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2bf3-108">Return value</span></span>

<span data-ttu-id="f2bf3-109">Restituisce \_ OK se il renderer utilizza l'origine predefinita; in caso contrario, restituisce \_ false.</span><span class="sxs-lookup"><span data-stu-id="f2bf3-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bf3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2bf3-110">Requirements</span></span>



| <span data-ttu-id="f2bf3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2bf3-111">Requirement</span></span> | <span data-ttu-id="f2bf3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f2bf3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bf3-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2bf3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f2bf3-114"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf3-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2bf3-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2bf3-115">Library</span></span><br/> | <dl> <span data-ttu-id="f2bf3-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2bf3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2bf3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2bf3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bf3-118">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f2bf3-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




