---
description: Il metodo IsNormalRate indica se la clip viene riprodotto alla frequenza di riproduzione normale; ovvero la velocità di riproduzione del file originale.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Metodo IAMTimelineSrc:: IsNormalRate (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332752"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="ce49c-103">Metodo IAMTimelineSrc:: IsNormalRate</span><span class="sxs-lookup"><span data-stu-id="ce49c-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="ce49c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ce49c-104">\[Deprecated.</span></span> <span data-ttu-id="ce49c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce49c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ce49c-106">Il `IsNormalRate` metodo indica se il clip verrà riprodotto alla frequenza di riproduzione normale, ovvero la velocità di riproduzione del file originale.</span><span class="sxs-lookup"><span data-stu-id="ce49c-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce49c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce49c-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ce49c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce49c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce49c-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="ce49c-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ce49c-110">Riceve un valore booleano che indica come viene eseguito il rendering della clip.</span><span class="sxs-lookup"><span data-stu-id="ce49c-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="ce49c-111">Se il valore è **true**, il clip verrà riprodotto alla tariffa normale.</span><span class="sxs-lookup"><span data-stu-id="ce49c-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="ce49c-112">In caso contrario, verrà riprodotto più veloce o più lento del normale.</span><span class="sxs-lookup"><span data-stu-id="ce49c-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce49c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce49c-113">Return value</span></span>

<span data-ttu-id="ce49c-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ce49c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce49c-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce49c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce49c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce49c-116">Remarks</span></span>

<span data-ttu-id="ce49c-117">La velocità di riproduzione di una clip è determinata dalle ore di inizio e di fine del supporto, in relazione ai tempi di sequenza temporale:</span><span class="sxs-lookup"><span data-stu-id="ce49c-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="ce49c-118">Se questo rapporto è uguale a 1, il clip viene riprodotto alla velocità creata.</span><span class="sxs-lookup"><span data-stu-id="ce49c-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="ce49c-119">In caso contrario, viene riprodotto più velocemente o più lentamente.</span><span class="sxs-lookup"><span data-stu-id="ce49c-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="ce49c-120">Per ulteriori informazioni, vedere [tempo in servizi di modifica DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ce49c-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="ce49c-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ce49c-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce49c-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce49c-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ce49c-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ce49c-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce49c-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce49c-124">Requirements</span></span>



| <span data-ttu-id="ce49c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce49c-125">Requirement</span></span> | <span data-ttu-id="ce49c-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ce49c-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce49c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce49c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ce49c-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce49c-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ce49c-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce49c-129">Library</span></span><br/> | <dl> <span data-ttu-id="ce49c-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce49c-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce49c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce49c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce49c-132">**Interfaccia IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="ce49c-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ce49c-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ce49c-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




