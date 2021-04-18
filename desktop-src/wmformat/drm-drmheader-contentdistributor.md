---
title: DRM_DRMHeader_ContentDistributor
description: L' \_ attributo contentdistributor di DRM DRMHeader \_ contiene una stringa identifiying il server di distribuzione del contenuto.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299449"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="6babe-104">\_Contentdistributor DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="6babe-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="6babe-105">L' **attributo \_ \_ contentdistributor di DRM DRMHeader** contiene una stringa identifiying il server di distribuzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6babe-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6babe-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="6babe-106">Global Constant</span></span>

<span data-ttu-id="6babe-107">g \_ wszWMDRM \_ DRMHeader \_ contentdistributor</span><span class="sxs-lookup"><span data-stu-id="6babe-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="6babe-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6babe-108">Data Type</span></span>

<span data-ttu-id="6babe-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="6babe-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="6babe-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6babe-110">Remarks</span></span>

<span data-ttu-id="6babe-111">L'ID contenuto è facoltativo e viene determinato esclusivamente dall'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6babe-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="6babe-112">L'oggetto writer non esegue alcuna operazione con questo attributo.</span><span class="sxs-lookup"><span data-stu-id="6babe-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="6babe-113">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="6babe-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="6babe-114">Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="6babe-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="6babe-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6babe-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6babe-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="6babe-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




