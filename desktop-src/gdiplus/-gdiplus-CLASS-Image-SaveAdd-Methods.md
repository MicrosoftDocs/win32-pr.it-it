---
description: In questo argomento vengono elencati i metodi SaveAdd della classe Image. Per un elenco completo dei metodi per la classe Image, vedere Metodi di immagine.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Metodi Image. SaveAdd (Gdiplusheaders. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979314"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="ef2cb-104">Metodi Image. SaveAdd</span><span class="sxs-lookup"><span data-stu-id="ef2cb-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="ef2cb-105">In questo argomento vengono elencati i metodi SaveAdd della classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="ef2cb-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="ef2cb-106">Per un elenco completo dei metodi per la classe **Image** , vedere [metodi di immagine](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ef2cb-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="ef2cb-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="ef2cb-107">Overload list</span></span>



| <span data-ttu-id="ef2cb-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="ef2cb-108">Method</span></span>                                                                                               | <span data-ttu-id="ef2cb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef2cb-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2cb-110">[**SaveAdd (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ef2cb-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="ef2cb-111">Il metodo [**Image:: SaveAdd**](/previous-versions//ms535408(v=vs.85)) aggiunge un frame a un file o a un flusso specificato in una chiamata precedente al metodo **Save** .</span><span class="sxs-lookup"><span data-stu-id="ef2cb-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="ef2cb-112">Usare questo metodo per salvare i fotogrammi selezionati da un'immagine a più fotogrammi in un'altra immagine a più fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="ef2cb-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="ef2cb-113">[**SaveAdd (Image \* , EncoderParameters \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="ef2cb-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="ef2cb-114">Il metodo [**Image:: SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) aggiunge un frame a un file o a un flusso specificato in una chiamata precedente al metodo **Save** .</span><span class="sxs-lookup"><span data-stu-id="ef2cb-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="ef2cb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef2cb-115">Requirements</span></span>



| <span data-ttu-id="ef2cb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2cb-116">Requirement</span></span> | <span data-ttu-id="ef2cb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ef2cb-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2cb-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef2cb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ef2cb-119">Solo app desktop Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="ef2cb-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ef2cb-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef2cb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ef2cb-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef2cb-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ef2cb-122">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ef2cb-122">Product</span></span><br/>                  | <span data-ttu-id="ef2cb-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="ef2cb-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="ef2cb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef2cb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef2cb-125"><dt>Gdiplusheaders. h (include Gdiplus. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef2cb-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="ef2cb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef2cb-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef2cb-127"><dt>Gdiplus. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef2cb-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
