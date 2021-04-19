---
description: Metodo del costruttore.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Costruttore CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325939"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="f2d61-103">Costruttore CBaseControlWindow. CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="f2d61-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="f2d61-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="f2d61-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2d61-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f2d61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2d61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2d61-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="f2d61-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d61-108">Puntatore all'oggetto filtro multimediale proprietario.</span><span class="sxs-lookup"><span data-stu-id="f2d61-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="f2d61-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="f2d61-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d61-110">Puntatore alla sezione critica da usare per il blocco.</span><span class="sxs-lookup"><span data-stu-id="f2d61-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="f2d61-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="f2d61-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d61-112">Puntatore alla descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f2d61-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="f2d61-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f2d61-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d61-114">Puntatore all'interfaccia **IUnknown** di controllo, se l'oggetto fa parte di un'aggregazione. in caso contrario, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="f2d61-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f2d61-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="f2d61-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f2d61-116">Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="f2d61-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2d61-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2d61-117">Requirements</span></span>



| <span data-ttu-id="f2d61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2d61-118">Requirement</span></span> | <span data-ttu-id="f2d61-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f2d61-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2d61-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2d61-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f2d61-121"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2d61-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2d61-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2d61-122">Library</span></span><br/> | <dl> <span data-ttu-id="f2d61-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2d61-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2d61-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2d61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2d61-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="f2d61-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




