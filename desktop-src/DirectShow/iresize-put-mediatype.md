---
description: Il \_ metodo Put MediaType imposta il tipo di supporto di output sul filtro Resizer.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: metodo:p ut_MediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327327"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="64065-103">IResize::p UT \_ mediaType metodo</span><span class="sxs-lookup"><span data-stu-id="64065-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="64065-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="64065-104">\[Deprecated.</span></span> <span data-ttu-id="64065-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64065-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="64065-106">Il `put_MediaType` metodo imposta il tipo di supporto di output sul filtro Resizer.</span><span class="sxs-lookup"><span data-stu-id="64065-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="64065-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64065-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="64065-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="64065-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64065-109">*PMT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64065-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64065-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="64065-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64065-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64065-111">Return value</span></span>

<span data-ttu-id="64065-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64065-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64065-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64065-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64065-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="64065-114">Remarks</span></span>

<span data-ttu-id="64065-115">DES chiama questo metodo prima di connettere il pin di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="64065-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="64065-116">Usare il tipo di supporto come tipo di supporto del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="64065-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="64065-117">Restituire questo tipo di supporto nel metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) e selezionare contro questo tipo nel metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="64065-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="64065-118">DES non chiama mai questo metodo dopo la connessione del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="64065-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="64065-119">Attualmente, DES imposta sempre il tipo di supporto di output su un formato RGB non compresso con un blocco di formato **VIDEOINFOHEADER** (il tipo di formato è uguale a Format \_ videoinfo).</span><span class="sxs-lookup"><span data-stu-id="64065-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="64065-120">Il sottotipo potrebbe essere MEDIASUBTYPE \_ ARGB32, che indica RGB a 32 bit con un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="64065-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="64065-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="64065-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="64065-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="64065-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="64065-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="64065-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64065-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64065-124">Requirements</span></span>



| <span data-ttu-id="64065-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="64065-125">Requirement</span></span> | <span data-ttu-id="64065-126">Valore</span><span class="sxs-lookup"><span data-stu-id="64065-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64065-127">Versione</span><span class="sxs-lookup"><span data-stu-id="64065-127">Version</span></span><br/> | <span data-ttu-id="64065-128">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="64065-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="64065-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64065-129">Header</span></span><br/>  | <dl> <span data-ttu-id="64065-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="64065-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="64065-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="64065-131">Library</span></span><br/> | <dl> <span data-ttu-id="64065-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64065-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64065-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64065-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64065-134">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="64065-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="64065-135">**Interfaccia IResize**</span><span class="sxs-lookup"><span data-stu-id="64065-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




