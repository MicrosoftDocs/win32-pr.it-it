---
description: Il \_ metodo Get FullScreenMode recupera la modalità a schermo intero corrente.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Metodo CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329869"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="121ad-103">Metodo CBaseControlWindow. Get \_ FullScreenMode</span><span class="sxs-lookup"><span data-stu-id="121ad-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="121ad-104">Il `get_FullScreenMode` metodo recupera la modalità a schermo intero corrente.</span><span class="sxs-lookup"><span data-stu-id="121ad-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="121ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="121ad-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="121ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="121ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="121ad-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="121ad-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="121ad-108">Puntatore alla modalità a schermo intero corrente.</span><span class="sxs-lookup"><span data-stu-id="121ad-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="121ad-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="121ad-109">Return value</span></span>

<span data-ttu-id="121ad-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="121ad-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="121ad-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="121ad-111">Remarks</span></span>

<span data-ttu-id="121ad-112">Questa funzione membro restituisce E \_ NOTIMPL per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="121ad-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="121ad-113">In questo modo si informa il server di distribuzione plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) che questo renderer non implementa un renderer a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="121ad-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="121ad-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="121ad-114">Requirements</span></span>



| <span data-ttu-id="121ad-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="121ad-115">Requirement</span></span> | <span data-ttu-id="121ad-116">Valore</span><span class="sxs-lookup"><span data-stu-id="121ad-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="121ad-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="121ad-117">Header</span></span><br/>  | <dl> <span data-ttu-id="121ad-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="121ad-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="121ad-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="121ad-119">Library</span></span><br/> | <dl> <span data-ttu-id="121ad-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="121ad-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="121ad-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="121ad-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121ad-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="121ad-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




