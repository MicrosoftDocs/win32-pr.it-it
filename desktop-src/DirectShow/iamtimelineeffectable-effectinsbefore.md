---
description: Il metodo EffectInsBefore inserisce un effetto nell'oggetto al livello di priorità specificato.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Metodo IAMTimelineEffectable:: EffectInsBefore (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333697"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="549a4-103">Metodo IAMTimelineEffectable:: EffectInsBefore</span><span class="sxs-lookup"><span data-stu-id="549a4-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="549a4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="549a4-104">\[Deprecated.</span></span> <span data-ttu-id="549a4-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="549a4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="549a4-106">Il `EffectInsBefore` metodo inserisce un effetto nell'oggetto al livello di priorità specificato.</span><span class="sxs-lookup"><span data-stu-id="549a4-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="549a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="549a4-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="549a4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="549a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549a4-109">*pFX*</span><span class="sxs-lookup"><span data-stu-id="549a4-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="549a4-110">Puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="549a4-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="549a4-111">*Priorità*</span><span class="sxs-lookup"><span data-stu-id="549a4-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="549a4-112">Livello di priorità in corrispondenza del quale inserire l'effetto.</span><span class="sxs-lookup"><span data-stu-id="549a4-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="549a4-113">Usare il valore-1 per inserire l'effetto alla fine dell'elenco di priorità.</span><span class="sxs-lookup"><span data-stu-id="549a4-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549a4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="549a4-114">Return value</span></span>

<span data-ttu-id="549a4-115">Restituisce \_ OK se ha esito positivo o E \_ NOTIMPL se l'oggetto non è un effetto.</span><span class="sxs-lookup"><span data-stu-id="549a4-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="549a4-116">In caso contrario, restituisce un altro valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="549a4-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="549a4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="549a4-117">Remarks</span></span>

<span data-ttu-id="549a4-118">Se necessario, le ore di inizio e di fine dell'effetto vengono ritagliate entro i limiti dell'intervallo di tempo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="549a4-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="549a4-119">Se è già presente un effetto al livello di priorità specificato, tutti gli effetti dal punto in poi spostano verso il basso l'elenco delle priorità per fare spazio al nuovo effetto.</span><span class="sxs-lookup"><span data-stu-id="549a4-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="549a4-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="549a4-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="549a4-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="549a4-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="549a4-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="549a4-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="549a4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="549a4-123">Requirements</span></span>



| <span data-ttu-id="549a4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="549a4-124">Requirement</span></span> | <span data-ttu-id="549a4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="549a4-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="549a4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="549a4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="549a4-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="549a4-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="549a4-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="549a4-128">Library</span></span><br/> | <dl> <span data-ttu-id="549a4-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="549a4-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="549a4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="549a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="549a4-131">**Interfaccia IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="549a4-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="549a4-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="549a4-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




