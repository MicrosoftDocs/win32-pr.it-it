---
description: 'Costruttore CBaseControlWindow.CBaseControlWindow : metodo costruttore.'
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Costruttore CBaseControlWindow.CBaseControlWindow (Ctlutil.h)
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
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096339"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="d72cd-103">Costruttore CBaseControlWindow.CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="d72cd-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="d72cd-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d72cd-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d72cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d72cd-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d72cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d72cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72cd-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="d72cd-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="d72cd-108">Puntatore all'oggetto filtro multimediale proprietario.</span><span class="sxs-lookup"><span data-stu-id="d72cd-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="d72cd-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="d72cd-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="d72cd-110">Puntatore alla sezione critica da usare per il blocco.</span><span class="sxs-lookup"><span data-stu-id="d72cd-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="d72cd-111">*Pname*</span><span class="sxs-lookup"><span data-stu-id="d72cd-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d72cd-112">Puntatore alla descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d72cd-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="d72cd-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="d72cd-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d72cd-114">Puntatore **all'interfaccia IUnknown di** controllo, se l'oggetto fa parte di un'aggregazione; in caso contrario, deve essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d72cd-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d72cd-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="d72cd-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d72cd-116">Puntatore a una variabile che riceve un valore HRESULT che indica l'esito positivo o negativo del metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d72cd-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d72cd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d72cd-117">Requirements</span></span>



| <span data-ttu-id="d72cd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d72cd-118">Requirement</span></span> | <span data-ttu-id="d72cd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d72cd-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d72cd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d72cd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d72cd-121"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d72cd-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d72cd-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="d72cd-122">Library</span></span><br/> | <dl> <span data-ttu-id="d72cd-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d72cd-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d72cd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d72cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72cd-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="d72cd-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




