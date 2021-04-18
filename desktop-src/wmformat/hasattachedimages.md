---
title: HasAttachedImages
description: L'attributo HasAttachedImages è un attributo a livello di file che specifica se il file è un file MP3 con frame ID3 ad APIC collegati.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages Windows Media Format
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299411"
---
# <a name="hasattachedimages"></a><span data-ttu-id="1b36e-104">HasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="1b36e-104">HasAttachedImages</span></span>

<span data-ttu-id="1b36e-105">L'attributo **HasAttachedImages** è un attributo a livello di file che specifica se il file è un file MP3 con frame ID3 ad APIC collegati.</span><span class="sxs-lookup"><span data-stu-id="1b36e-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1b36e-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="1b36e-106">Global Constant</span></span>

<span data-ttu-id="1b36e-107">g \_ wszWMHasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="1b36e-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="1b36e-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1b36e-108">Data Type</span></span>

<span data-ttu-id="1b36e-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1b36e-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="1b36e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b36e-110">Remarks</span></span>

<span data-ttu-id="1b36e-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="1b36e-111">This is a coded attribute.</span></span>

<span data-ttu-id="1b36e-112">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="1b36e-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="1b36e-113">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1b36e-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="1b36e-114">**HasAttachedImages** è stato progettato per informare un'applicazione che erano presenti immagini in modo che potessero essere recuperate usando l'interfaccia [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) .</span><span class="sxs-lookup"><span data-stu-id="1b36e-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="1b36e-115">Ora che le immagini sono supportate usando l'attributo [**WM/Picture**](wmpicture.md) , **HasAttachedImages** non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="1b36e-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="1b36e-116">Per determinare se un file contiene immagini, chiamare [**IWMHeaderInfo3:: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specificando l'attributo **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="1b36e-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b36e-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b36e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b36e-118">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="1b36e-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




