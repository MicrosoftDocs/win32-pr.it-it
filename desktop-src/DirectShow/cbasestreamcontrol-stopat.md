---
description: 'Il metodo StopAt informa il PIN quando interrompere la distribuzione dei dati. Questo metodo implementa il metodo IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Metodo CBaseStreamControl. StopAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324026"
---
# <a name="cbasestreamcontrolstopat-method"></a><span data-ttu-id="325c1-104">CBaseStreamControl. StopAt, metodo</span><span class="sxs-lookup"><span data-stu-id="325c1-104">CBaseStreamControl.StopAt method</span></span>

<span data-ttu-id="325c1-105">Il `StopAt` metodo informa il PIN quando interrompere la distribuzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="325c1-105">The `StopAt` method informs the pin when to stop delivering data.</span></span> <span data-ttu-id="325c1-106">Questo metodo implementa il metodo [**IAMStreamControl:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="325c1-106">This method implements the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="325c1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="325c1-107">Syntax</span></span>


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="325c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="325c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325c1-109">*ptStop*</span><span class="sxs-lookup"><span data-stu-id="325c1-109">*ptStop*</span></span> 
</dt> <dd>

<span data-ttu-id="325c1-110">Puntatore a un valore di [**\_ ora di riferimento**](reference-time.md) che specifica quando il PIN deve interrompere la distribuzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="325c1-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should stop delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="325c1-111">*bSendExtra*</span><span class="sxs-lookup"><span data-stu-id="325c1-111">*bSendExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="325c1-112">Specifica un valore booleano che indica se inviare un campione aggiuntivo dopo l'ora di arresto pianificata.</span><span class="sxs-lookup"><span data-stu-id="325c1-112">Specifies a Boolean value that indicates whether to send an extra sample after the scheduled stop time.</span></span> <span data-ttu-id="325c1-113">Se **true**, il pin Invia un campione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="325c1-113">If **TRUE**, the pin sends one extra sample.</span></span>

</dd> <dt>

<span data-ttu-id="325c1-114">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="325c1-114">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="325c1-115">Specifica un valore da inviare insieme alla notifica di avvio.</span><span class="sxs-lookup"><span data-stu-id="325c1-115">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325c1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="325c1-116">Return value</span></span>

<span data-ttu-id="325c1-117">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="325c1-117">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="325c1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="325c1-118">Requirements</span></span>



| <span data-ttu-id="325c1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="325c1-119">Requirement</span></span> | <span data-ttu-id="325c1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="325c1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="325c1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="325c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="325c1-122"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="325c1-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="325c1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="325c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="325c1-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="325c1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="325c1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="325c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325c1-126">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="325c1-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




