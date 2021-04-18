---
description: Il metodo GetGroup recupera un gruppo specificato.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'Metodo IAMTimeline:: GetGroup (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325639"
---
# <a name="iamtimelinegetgroup-method"></a><span data-ttu-id="d1361-103">Metodo IAMTimeline:: GetGroup</span><span class="sxs-lookup"><span data-stu-id="d1361-103">IAMTimeline::GetGroup method</span></span>

> [!Note]  
> <span data-ttu-id="d1361-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d1361-104">\[Deprecated.</span></span> <span data-ttu-id="d1361-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1361-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d1361-106">Il `GetGroup` metodo recupera un gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="d1361-106">The `GetGroup` method retrieves a specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1361-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1361-107">Syntax</span></span>


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a><span data-ttu-id="d1361-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1361-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1361-109">*ppGroup* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d1361-109">*ppGroup* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1361-110">Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d1361-110">Receives a pointer to the group's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1361-111">*WhichGroup*</span><span class="sxs-lookup"><span data-stu-id="d1361-111">*WhichGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="d1361-112">Indice del gruppo da recuperare in base all'ordine in cui i gruppi sono stati aggiunti alla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="d1361-112">Index of the group to retrieve, based on the order in which the groups were added to the timeline.</span></span> <span data-ttu-id="d1361-113">Il primo gruppo aggiunto alla sequenza temporale ha un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="d1361-113">The first group added to the timeline has an index of 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1361-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1361-114">Return value</span></span>

<span data-ttu-id="d1361-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d1361-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1361-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1361-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1361-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1361-117">Remarks</span></span>

<span data-ttu-id="d1361-118">Se il metodo ha esito positivo, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="d1361-118">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="d1361-119">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="d1361-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="d1361-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d1361-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d1361-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1361-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d1361-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d1361-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d1361-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1361-123">Requirements</span></span>



| <span data-ttu-id="d1361-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1361-124">Requirement</span></span> | <span data-ttu-id="d1361-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d1361-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1361-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1361-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d1361-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1361-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d1361-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1361-128">Library</span></span><br/> | <dl> <span data-ttu-id="d1361-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1361-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1361-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1361-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1361-131">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="d1361-131">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d1361-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d1361-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




