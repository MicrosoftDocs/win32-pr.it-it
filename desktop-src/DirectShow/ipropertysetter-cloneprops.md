---
description: Il metodo CloneProps clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Metodo IPropertySetter:: CloneProps (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325482"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="75ee6-103">Metodo IPropertySetter:: CloneProps</span><span class="sxs-lookup"><span data-stu-id="75ee6-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="75ee6-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="75ee6-104">\[Deprecated.</span></span> <span data-ttu-id="75ee6-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75ee6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="75ee6-106">Il `CloneProps` metodo clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.</span><span class="sxs-lookup"><span data-stu-id="75ee6-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ee6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75ee6-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="75ee6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75ee6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ee6-109">*ppSetter* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="75ee6-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75ee6-110">Riceve un puntatore all'interfaccia **IPropertySetter** del nuovo setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="75ee6-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="75ee6-111">*rtStart* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75ee6-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ee6-112">Ora di inizio dell'intervallo di valori da clonare, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="75ee6-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="75ee6-113">*rtStop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75ee6-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ee6-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="75ee6-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ee6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75ee6-115">Return value</span></span>

<span data-ttu-id="75ee6-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="75ee6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75ee6-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75ee6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ee6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ee6-118">Remarks</span></span>

<span data-ttu-id="75ee6-119">Vengono clonati solo i valori che rientrano dopo l'ora di inizio specificata.</span><span class="sxs-lookup"><span data-stu-id="75ee6-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="75ee6-120">Gli orari dei valori clonati vengono quindi modificati rispetto all'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="75ee6-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="75ee6-121">Ad esempio, se *rtStart* è 20 milioni (2 secondi), un valore all'ora 30 milioni (3 secondi) viene clonato con l'ora 10 milioni (1 secondo).</span><span class="sxs-lookup"><span data-stu-id="75ee6-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="75ee6-122">Infine, a ogni proprietà clonata viene assegnato un valore iniziale uguale al valore della proprietà originale all'ora di inizio (interpolate correttamente, se necessario).</span><span class="sxs-lookup"><span data-stu-id="75ee6-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="75ee6-123">I dati della proprietà vengono in effetti divisi all'ora di inizio specificata.</span><span class="sxs-lookup"><span data-stu-id="75ee6-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="75ee6-124">Se il metodo ha esito positivo, l'interfaccia [**IPropertySetter**](ipropertysetter.md) restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="75ee6-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="75ee6-125">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="75ee6-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="75ee6-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="75ee6-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="75ee6-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="75ee6-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="75ee6-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="75ee6-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="75ee6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ee6-129">Requirements</span></span>



| <span data-ttu-id="75ee6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ee6-130">Requirement</span></span> | <span data-ttu-id="75ee6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="75ee6-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ee6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75ee6-132">Header</span></span><br/>  | <dl> <span data-ttu-id="75ee6-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ee6-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="75ee6-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="75ee6-134">Library</span></span><br/> | <dl> <span data-ttu-id="75ee6-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75ee6-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ee6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ee6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ee6-137">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="75ee6-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="75ee6-138">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="75ee6-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




