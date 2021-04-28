---
description: Costruttore CRendererPosPassThru.CRendererPosPassThru - Metodo costruttore.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Costruttore CRendererPosPassThru.CRendererPosPassThru (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59972f12f0f746ef68c267e3fbd0d071d54193c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085409"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="84847-103">Costruttore CRendererPosPassThru.CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="84847-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="84847-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="84847-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="84847-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84847-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="84847-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84847-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="84847-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="84847-108">Puntatore al nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="84847-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="84847-109">Allocare questo parametro nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="84847-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="84847-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="84847-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="84847-111">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="84847-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="84847-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** aggregatore.</span><span class="sxs-lookup"><span data-stu-id="84847-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="84847-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="84847-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="84847-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="84847-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="84847-115">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="84847-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="84847-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="84847-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="84847-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="84847-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="84847-118">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="84847-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84847-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84847-119">Requirements</span></span>



| <span data-ttu-id="84847-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84847-120">Requirement</span></span> | <span data-ttu-id="84847-121">Valore</span><span class="sxs-lookup"><span data-stu-id="84847-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84847-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84847-122">Header</span></span><br/>  | <dl> <span data-ttu-id="84847-123"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="84847-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84847-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="84847-124">Library</span></span><br/> | <dl> <span data-ttu-id="84847-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84847-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




