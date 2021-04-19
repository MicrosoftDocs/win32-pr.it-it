---
description: Metodo del costruttore.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Costruttore CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327584"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="0e40a-103">Costruttore CBaseControlVideo. CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="0e40a-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="0e40a-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0e40a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e40a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e40a-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0e40a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e40a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e40a-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="0e40a-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0e40a-108">Puntatore all'oggetto filtro multimediale proprietario.</span><span class="sxs-lookup"><span data-stu-id="0e40a-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="0e40a-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="0e40a-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0e40a-110">Puntatore alla sezione critica da usare per il blocco.</span><span class="sxs-lookup"><span data-stu-id="0e40a-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="0e40a-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="0e40a-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0e40a-112">Puntatore alla descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e40a-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="0e40a-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0e40a-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0e40a-114">Puntatore all'interfaccia **IUnknown** di controllo, se l'oggetto fa parte di un'aggregazione. in caso contrario, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0e40a-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e40a-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="0e40a-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0e40a-116">Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="0e40a-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e40a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e40a-117">Remarks</span></span>

<span data-ttu-id="0e40a-118">L'oggetto implementa l'interfaccia di controllo [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="0e40a-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="0e40a-119">Tutti i metodi di interfaccia di [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) implementati da questa classe richiedono che il filtro sia connesso correttamente.</span><span class="sxs-lookup"><span data-stu-id="0e40a-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="0e40a-120">Per questo motivo, alla classe viene passato un pin con il quale deve essere sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="0e40a-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="0e40a-121">Ogni volta che viene chiamato un metodo di interfaccia, l'oggetto determina che il PIN è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="0e40a-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e40a-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e40a-122">Requirements</span></span>



| <span data-ttu-id="0e40a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e40a-123">Requirement</span></span> | <span data-ttu-id="0e40a-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0e40a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e40a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e40a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0e40a-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e40a-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0e40a-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e40a-127">Library</span></span><br/> | <dl> <span data-ttu-id="0e40a-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0e40a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e40a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e40a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e40a-130">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="0e40a-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




