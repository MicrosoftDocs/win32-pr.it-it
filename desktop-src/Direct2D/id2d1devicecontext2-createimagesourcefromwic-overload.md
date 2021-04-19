---
title: Metodi CreateImageSourceFromWic di ID2D1DeviceContext2 (D2d1 \_ 3. h)
description: Consente di creare un oggetto di origine immagine da un'origine bitmap WIC, durante il popolamento di tutta la memoria pixel all'interno dell'origine dell'immagine. L'immagine viene caricata e archiviata con una quantità minima di memoria.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Metodo CreateImageSourceFromWic Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333017"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="0f887-105">Metodi ID2D1DeviceContext2:: CreateImageSourceFromWic</span><span class="sxs-lookup"><span data-stu-id="0f887-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="0f887-106">Consente di creare un oggetto di origine immagine da un'origine bitmap WIC, durante il popolamento di tutta la memoria pixel all'interno dell'origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0f887-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="0f887-107">L'immagine viene caricata e archiviata con una quantità minima di memoria.</span><span class="sxs-lookup"><span data-stu-id="0f887-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="0f887-108">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="0f887-108">Overload list</span></span>



| <span data-ttu-id="0f887-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="0f887-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="0f887-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f887-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f887-111">[**CreateImageSourceFromWic (IWICBitmapSource \* , d2d1 \_ Image \_ source \_ Loading \_ options, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="0f887-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="0f887-112">Versione del metodo che consente di specificare l'origine della bitmap WIC, l'oggetto di origine dell'immagine di output e le opzioni di caricamento con la modalità Alpha predefinita.</span><span class="sxs-lookup"><span data-stu-id="0f887-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="0f887-113">[**CreateImageSourceFromWic (IWICBitmapSource \* , d2d1 \_ Image \_ source \_ Loading \_ options, d2d1 \_ Alpha \_ mode, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="0f887-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="0f887-114">Versione del metodo che consente di specificare l'origine della bitmap WIC, l'oggetto di origine dell'immagine di output e le opzioni di caricamento e la modalità Alpha.</span><span class="sxs-lookup"><span data-stu-id="0f887-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="0f887-115">[**CreateImageSourceFromWic (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="0f887-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="0f887-116">Versione del metodo che consente di specificare l'origine della bitmap WIC e l'oggetto di origine dell'immagine di output con opitons di caricamento predefinito e la modalità Alpha.</span><span class="sxs-lookup"><span data-stu-id="0f887-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0f887-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f887-117">Requirements</span></span>



| <span data-ttu-id="0f887-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f887-118">Requirement</span></span> | <span data-ttu-id="0f887-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0f887-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f887-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f887-120">Header</span></span><br/> | <dl> <span data-ttu-id="0f887-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f887-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f887-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f887-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f887-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="0f887-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="0f887-124">�</span><span class="sxs-lookup"><span data-stu-id="0f887-124">�</span></span>

<span data-ttu-id="0f887-125">�</span><span class="sxs-lookup"><span data-stu-id="0f887-125">�</span></span>
