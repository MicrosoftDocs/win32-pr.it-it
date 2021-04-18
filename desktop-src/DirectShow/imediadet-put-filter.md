---
description: Il \_ metodo Put Filter specifica un filtro di origine per il rilevamento multimediale da usare.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet: metodo:p ut_Filter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327822"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="6d0f9-103">IMediaDet: metodo di \_ filtro ut:p</span><span class="sxs-lookup"><span data-stu-id="6d0f9-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="6d0f9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-104">\[Deprecated.</span></span> <span data-ttu-id="6d0f9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d0f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d0f9-106">Il `put_Filter` metodo specifica un filtro di origine per il rilevamento multimediale da usare.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d0f9-107">Non aggiungere il filtro di origine al grafico di filtro oppure usare un filtro già presente in un grafico a filtro.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="6d0f9-108">L'oggetto Media Detector compila automaticamente un grafico di filtro interno e l'inserimento del filtro in un altro grafico può causare risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6d0f9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d0f9-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d0f9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d0f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0f9-111">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d0f9-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0f9-112">Puntatore all'interfaccia **IUnknown** del filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0f9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d0f9-113">Return value</span></span>

<span data-ttu-id="6d0f9-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d0f9-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6d0f9-115">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d0f9-115">Possible values include the following:</span></span>



| <span data-ttu-id="6d0f9-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6d0f9-116">Return code</span></span>                                                                                   | <span data-ttu-id="6d0f9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d0f9-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6d0f9-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f9-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6d0f9-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="6d0f9-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f9-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="6d0f9-121">*newVal* non punta a un filtro.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="6d0f9-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f9-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6d0f9-123">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="6d0f9-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="6d0f9-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d0f9-124">Remarks</span></span>

<span data-ttu-id="6d0f9-125">Per la maggior parte delle applicazioni, è più semplice chiamare il metodo [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) con il nome di un file di origine.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="6d0f9-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d0f9-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d0f9-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d0f9-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6d0f9-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d0f9-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d0f9-129">Requirements</span></span>



| <span data-ttu-id="6d0f9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d0f9-130">Requirement</span></span> | <span data-ttu-id="6d0f9-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6d0f9-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0f9-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d0f9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="6d0f9-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f9-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d0f9-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d0f9-134">Library</span></span><br/> | <dl> <span data-ttu-id="6d0f9-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d0f9-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0f9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d0f9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0f9-137">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="6d0f9-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="6d0f9-138">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6d0f9-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




