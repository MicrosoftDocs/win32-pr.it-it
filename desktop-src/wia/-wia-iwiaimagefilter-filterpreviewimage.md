---
description: Filtra l'immagine di anteprima.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Metodo IWiaImageFilter:: FilterPreviewImage (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308223"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="15331-103">Metodo IWiaImageFilter:: FilterPreviewImage</span><span class="sxs-lookup"><span data-stu-id="15331-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="15331-104">Filtra l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="15331-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="15331-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15331-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="15331-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15331-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15331-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15331-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="15331-108">Type: **LONG**</span></span>

<span data-ttu-id="15331-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="15331-109">Not used.</span></span> <span data-ttu-id="15331-110">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="15331-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="15331-111">*pWiaChildItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15331-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15331-112">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="15331-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="15331-113">Elemento elaborato.</span><span class="sxs-lookup"><span data-stu-id="15331-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="15331-114">_InputImageExtents \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15331-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15331-115">Tipo: **Rect**</span><span class="sxs-lookup"><span data-stu-id="15331-115">Type: **RECT**</span></span>

<span data-ttu-id="15331-116">Coordinate (sull'area di acquisizione fisica) dell'immagine memorizzata internamente dal componente di anteprima.</span><span class="sxs-lookup"><span data-stu-id="15331-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="15331-117">*pInputStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15331-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15331-118">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="15331-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="15331-119">Puntatore all'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) per i dati dell'immagine memorizzati nella cache che vengono filtrati.</span><span class="sxs-lookup"><span data-stu-id="15331-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15331-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15331-120">Return value</span></span>

<span data-ttu-id="15331-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="15331-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="15331-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15331-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15331-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15331-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15331-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="15331-124">Remarks</span></span>

<span data-ttu-id="15331-125">Non chiamare questo metodo direttamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15331-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="15331-126">*pWiaChildItem2* deve essere un elemento figlio di *PWiaItem2* passato a [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="15331-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="15331-127">*InputImageExtents* è necessario perché il filtro di elaborazione delle immagini è responsabile del taglio dell'area immagine che *pWiaChildItem2* rappresenta dai dati dell'immagine passati attraverso *pInputStream*.</span><span class="sxs-lookup"><span data-stu-id="15331-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="15331-128">Un'applicazione deve garantire che *pWiaChildItem2* abbia lo stesso formato di immagine ( \_ formato ipa WIA \_ ), la risoluzione (WIA \_ IPS \_ XRES e WIA \_ IPS \_ YRES) e la profondità di bit (estensione \_ IPA WIA \_ ) come *pWiaItem2* aveva quando è stato passato in [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="15331-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15331-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15331-129">Requirements</span></span>



| <span data-ttu-id="15331-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="15331-130">Requirement</span></span> | <span data-ttu-id="15331-131">Valore</span><span class="sxs-lookup"><span data-stu-id="15331-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15331-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15331-132">Minimum supported client</span></span><br/> | <span data-ttu-id="15331-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15331-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15331-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15331-134">Minimum supported server</span></span><br/> | <span data-ttu-id="15331-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15331-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15331-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15331-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="15331-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="15331-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="15331-138">IDL</span><span class="sxs-lookup"><span data-stu-id="15331-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15331-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15331-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
