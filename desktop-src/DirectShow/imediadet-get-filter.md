---
description: Il \_ metodo Get Filter recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Metodo IMediaDet:: get_Filter (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331507"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="267f7-103">Metodo IMediaDet:: Get \_ Filter</span><span class="sxs-lookup"><span data-stu-id="267f7-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="267f7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="267f7-104">\[Deprecated.</span></span> <span data-ttu-id="267f7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="267f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="267f7-106">Il `get_Filter` metodo recupera un puntatore al filtro di origine attualmente utilizzato dal rilevamento multimediale.</span><span class="sxs-lookup"><span data-stu-id="267f7-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="267f7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="267f7-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="267f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="267f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="267f7-109">*ppVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="267f7-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="267f7-110">Riceve un puntatore all'interfaccia **IUnknown** del filtro.</span><span class="sxs-lookup"><span data-stu-id="267f7-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="267f7-111">Se non è in uso alcun filtro di origine, il valore viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="267f7-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="267f7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="267f7-112">Return value</span></span>

<span data-ttu-id="267f7-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="267f7-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="267f7-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="267f7-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="267f7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="267f7-115">Remarks</span></span>

<span data-ttu-id="267f7-116">Quando il metodo restituisce un risultato, se *\* ppVal* non è **null**, l'interfaccia **IUnknown** presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="267f7-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="267f7-117">Rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="267f7-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="267f7-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="267f7-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="267f7-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="267f7-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="267f7-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="267f7-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="267f7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="267f7-121">Requirements</span></span>



| <span data-ttu-id="267f7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="267f7-122">Requirement</span></span> | <span data-ttu-id="267f7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="267f7-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="267f7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="267f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="267f7-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="267f7-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="267f7-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="267f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="267f7-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="267f7-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267f7-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="267f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267f7-129">**Interfaccia IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="267f7-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="267f7-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="267f7-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




