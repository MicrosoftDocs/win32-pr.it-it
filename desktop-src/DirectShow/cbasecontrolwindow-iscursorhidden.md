---
description: Il metodo IsCursorHidden recupera lo stato corrente del \_ membro dati m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Metodo CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333614"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="baaef-103">CBaseControlWindow. IsCursorHidden, metodo</span><span class="sxs-lookup"><span data-stu-id="baaef-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="baaef-104">Il `IsCursorHidden` metodo recupera lo stato corrente del membro dati **m \_ bCursorHidden** .</span><span class="sxs-lookup"><span data-stu-id="baaef-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="baaef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baaef-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="baaef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="baaef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baaef-107">*CursorHidden*</span><span class="sxs-lookup"><span data-stu-id="baaef-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="baaef-108">Puntatore al valore di **m \_ bCursorHidden**.</span><span class="sxs-lookup"><span data-stu-id="baaef-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baaef-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="baaef-109">Return value</span></span>

<span data-ttu-id="baaef-110">Quando viene chiamato senza un parametro, restituisce OATRUE se il cursore è nascosto oppure OAFALSE se il cursore è visibile.</span><span class="sxs-lookup"><span data-stu-id="baaef-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="baaef-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="baaef-111">Remarks</span></span>

<span data-ttu-id="baaef-112">Gli oggetti interni devono chiamare questa funzione membro senza il parametro *CursorHidden* per evitare di bloccare la sezione critica.</span><span class="sxs-lookup"><span data-stu-id="baaef-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="baaef-113">Gli oggetti esterni accedono a questa funzione membro con il parametro *CursorHidden* tramite il metodo [**IVideoWindow:: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .</span><span class="sxs-lookup"><span data-stu-id="baaef-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="baaef-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baaef-114">Requirements</span></span>



| <span data-ttu-id="baaef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="baaef-115">Requirement</span></span> | <span data-ttu-id="baaef-116">Valore</span><span class="sxs-lookup"><span data-stu-id="baaef-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baaef-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baaef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="baaef-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baaef-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="baaef-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="baaef-119">Library</span></span><br/> | <dl> <span data-ttu-id="baaef-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="baaef-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baaef-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baaef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baaef-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="baaef-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




