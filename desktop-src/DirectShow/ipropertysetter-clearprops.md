---
description: Il Metodo ClearProps Cancella tutti i dati della proprietà dal setter della proprietà. L'applicazione può impostare i nuovi dati della proprietà dopo la chiamata a questa funzione.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Metodo IPropertySetter:: ClearProps (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325484"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="13ca0-104">Metodo IPropertySetter:: ClearProps</span><span class="sxs-lookup"><span data-stu-id="13ca0-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="13ca0-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="13ca0-105">\[Deprecated.</span></span> <span data-ttu-id="13ca0-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13ca0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13ca0-107">Il `ClearProps` metodo cancella tutti i dati della proprietà dal setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="13ca0-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="13ca0-108">L'applicazione può impostare i nuovi dati della proprietà dopo la chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="13ca0-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="13ca0-109">La cancellazione dei dati della proprietà non comporta il ripristino dei valori originali delle proprietà dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="13ca0-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="13ca0-110">Impedisce semplicemente a DirectShow di applicare eventuali altre modifiche.</span><span class="sxs-lookup"><span data-stu-id="13ca0-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="13ca0-111">I valori delle proprietà vengono applicati in fase di esecuzione quando viene eseguito il rendering del progetto.</span><span class="sxs-lookup"><span data-stu-id="13ca0-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ca0-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13ca0-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="13ca0-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="13ca0-113">Parameters</span></span>

<span data-ttu-id="13ca0-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="13ca0-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13ca0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13ca0-115">Return value</span></span>

<span data-ttu-id="13ca0-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="13ca0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13ca0-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13ca0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ca0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="13ca0-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="13ca0-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="13ca0-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="13ca0-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="13ca0-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="13ca0-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="13ca0-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13ca0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13ca0-122">Requirements</span></span>



| <span data-ttu-id="13ca0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ca0-123">Requirement</span></span> | <span data-ttu-id="13ca0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="13ca0-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13ca0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13ca0-125">Header</span></span><br/>  | <dl> <span data-ttu-id="13ca0-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ca0-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="13ca0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="13ca0-127">Library</span></span><br/> | <dl> <span data-ttu-id="13ca0-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13ca0-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13ca0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13ca0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ca0-130">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="13ca0-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="13ca0-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="13ca0-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




