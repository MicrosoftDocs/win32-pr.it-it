---
description: Costruttore CBaseControlVideo.CBaseControlVideo - Metodo costruttore.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Costruttore CBaseControlVideo.CBaseControlVideo (Ctlutil.h)
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
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096349"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="a9a01-103">Costruttore CBaseControlVideo.CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="a9a01-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="a9a01-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="a9a01-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9a01-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="a9a01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9a01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a01-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="a9a01-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a01-108">Puntatore all'oggetto filtro multimediale proprietario.</span><span class="sxs-lookup"><span data-stu-id="a9a01-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="a9a01-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="a9a01-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a01-110">Puntatore alla sezione critica da usare per il blocco.</span><span class="sxs-lookup"><span data-stu-id="a9a01-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="a9a01-111">*Pname*</span><span class="sxs-lookup"><span data-stu-id="a9a01-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a01-112">Puntatore alla descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a9a01-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="a9a01-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="a9a01-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a01-114">Puntatore **all'interfaccia IUnknown** di controllo, se l'oggetto fa parte di un'aggregazione; in caso contrario, deve essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a9a01-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9a01-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="a9a01-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a01-116">Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="a9a01-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9a01-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9a01-117">Remarks</span></span>

<span data-ttu-id="a9a01-118">L'oggetto implementa [**l'interfaccia di controllo IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo)</span><span class="sxs-lookup"><span data-stu-id="a9a01-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="a9a01-119">Tutti i metodi di interfaccia [**di IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) implementati da questa classe richiedono che il filtro sia connesso correttamente.</span><span class="sxs-lookup"><span data-stu-id="a9a01-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="a9a01-120">Per questo motivo, alla classe viene passato un pin con cui eseguire la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9a01-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="a9a01-121">Ogni volta che viene chiamato un metodo di interfaccia, l'oggetto determina che il pin è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="a9a01-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a01-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9a01-122">Requirements</span></span>



| <span data-ttu-id="a9a01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a01-123">Requirement</span></span> | <span data-ttu-id="a9a01-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a9a01-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a01-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9a01-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a9a01-126"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a01-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a9a01-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9a01-127">Library</span></span><br/> | <dl> <span data-ttu-id="a9a01-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a01-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a01-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9a01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a01-130">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="a9a01-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




