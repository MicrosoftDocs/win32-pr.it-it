---
description: "Il metodo FixTimes2 Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre. Questo metodo è equivalente a IAMTimelineObj:: FixTimes, ma accetta valori REFTIME."
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Metodo IAMTimelineObj:: FixTimes2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333586"
---
# <a name="iamtimelineobjfixtimes2-method"></a><span data-ttu-id="6106a-104">Metodo IAMTimelineObj:: FixTimes2</span><span class="sxs-lookup"><span data-stu-id="6106a-104">IAMTimelineObj::FixTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="6106a-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6106a-105">\[Deprecated.</span></span> <span data-ttu-id="6106a-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6106a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6106a-107">Il `FixTimes2` Metodo Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini, in base a quanto definito dall'impostazione della frequenza dei fotogrammi del gruppo padre.</span><span class="sxs-lookup"><span data-stu-id="6106a-107">The `FixTimes2` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span> <span data-ttu-id="6106a-108">Questo metodo è equivalente a [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md), ma accetta valori [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="6106a-108">This method is equivalent to [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6106a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6106a-109">Syntax</span></span>


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="6106a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6106a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6106a-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="6106a-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6106a-112">Puntatore a una variabile che contiene l'ora di inizio, in secondi.</span><span class="sxs-lookup"><span data-stu-id="6106a-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="6106a-113">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="6106a-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="6106a-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="6106a-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="6106a-115">Puntatore a una variabile che contiene l'ora di arresto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="6106a-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="6106a-116">Se la chiamata ha esito positivo, questa variabile viene impostata sul tempo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="6106a-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6106a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6106a-117">Return value</span></span>

<span data-ttu-id="6106a-118">Restituisce \_ OK se ha esito positivo o E \_ NOTINTREE se l'oggetto non fa parte di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="6106a-118">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="6106a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6106a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6106a-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6106a-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6106a-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6106a-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6106a-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6106a-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6106a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6106a-123">Requirements</span></span>



| <span data-ttu-id="6106a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6106a-124">Requirement</span></span> | <span data-ttu-id="6106a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6106a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6106a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6106a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6106a-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6106a-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6106a-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6106a-128">Library</span></span><br/> | <dl> <span data-ttu-id="6106a-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6106a-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6106a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6106a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6106a-131">**Interfaccia IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6106a-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6106a-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6106a-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




