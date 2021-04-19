---
description: Il \_ metodo Get MediaType restituisce il tipo di supporto di output corrente del filtro Resizer.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Metodo IResize:: get_MediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332569"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="dd567-103">Metodo IResize:: Get \_ mediaType</span><span class="sxs-lookup"><span data-stu-id="dd567-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="dd567-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd567-104">\[Deprecated.</span></span> <span data-ttu-id="dd567-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd567-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dd567-106">Il `get_MediaType` metodo restituisce il tipo di supporto di output corrente del filtro Resizer.</span><span class="sxs-lookup"><span data-stu-id="dd567-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd567-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd567-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="dd567-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd567-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd567-109">*PMT* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd567-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd567-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="dd567-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="dd567-111">Il metodo compila questa struttura con il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="dd567-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="dd567-112">Il chiamante deve rilasciare il blocco di formato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="dd567-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd567-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd567-113">Return value</span></span>

<span data-ttu-id="dd567-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd567-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd567-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd567-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd567-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd567-116">Remarks</span></span>

<span data-ttu-id="dd567-117">Se il tipo di supporto di output non è stato impostato, restituire un tipo di supporto predefinito.</span><span class="sxs-lookup"><span data-stu-id="dd567-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="dd567-118">Il filtro deve aggiornare il tipo di supporto di output quando vengono chiamati i metodi **put \_ mediaType** o **put \_ size** . il tipo di supporto restituito da `get_MediaType` deve riflettere queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="dd567-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="dd567-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="dd567-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dd567-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dd567-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dd567-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dd567-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd567-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd567-122">Requirements</span></span>



| <span data-ttu-id="dd567-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd567-123">Requirement</span></span> | <span data-ttu-id="dd567-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dd567-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd567-125">Versione</span><span class="sxs-lookup"><span data-stu-id="dd567-125">Version</span></span><br/> | <span data-ttu-id="dd567-126">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dd567-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="dd567-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd567-127">Header</span></span><br/>  | <dl> <span data-ttu-id="dd567-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd567-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dd567-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd567-129">Library</span></span><br/> | <dl> <span data-ttu-id="dd567-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd567-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd567-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd567-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd567-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="dd567-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="dd567-133">**Interfaccia IResize**</span><span class="sxs-lookup"><span data-stu-id="dd567-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




