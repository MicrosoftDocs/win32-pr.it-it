---
title: DRM_DRMHeader_SubscriptionContentID
description: L' \_ attributo DRM DRMHeader \_ SubscriptionContentID contiene l'ID contenuto della sottoscrizione.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956186"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="f461c-104">\_SubscriptionContentID DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="f461c-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="f461c-105">L'attributo **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contiene l'ID contenuto della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f461c-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f461c-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="f461c-106">Global Constant</span></span>

<span data-ttu-id="f461c-107">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="f461c-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="f461c-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f461c-108">Data Type</span></span>

<span data-ttu-id="f461c-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="f461c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f461c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f461c-110">Remarks</span></span>

<span data-ttu-id="f461c-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="f461c-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="f461c-112">L'ID contenuto della sottoscrizione è facoltativo e viene determinato esclusivamente dall'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="f461c-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="f461c-113">L'oggetto writer non esegue alcuna operazione con questo attributo.</span><span class="sxs-lookup"><span data-stu-id="f461c-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="f461c-114">Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="f461c-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="f461c-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f461c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f461c-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="f461c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




