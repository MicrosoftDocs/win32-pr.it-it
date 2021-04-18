---
title: DRM_DRMHeader_IndividualizedVersion
description: L' \_ attributo DRMHeaderIndividualizedVersion di DRM contiene la versione minima individualizzata richiesta per riprodurre il file.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299405"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="b25b7-104">\_IndividualizedVersion DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="b25b7-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="b25b7-105">L' **attributo \_ DRMHeaderIndividualizedVersion di DRM** contiene la versione minima individualizzata richiesta per riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="b25b7-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b25b7-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="b25b7-106">Global Constant</span></span>

<span data-ttu-id="b25b7-107">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="b25b7-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="b25b7-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b25b7-108">Data Type</span></span>

<span data-ttu-id="b25b7-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b25b7-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="b25b7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b25b7-110">Remarks</span></span>

<span data-ttu-id="b25b7-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="b25b7-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="b25b7-112">Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="b25b7-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="b25b7-113">Per impostare la versione individualizzata (detta anche versione di sicurezza) del file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , è necessario usare la proprietà [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) .</span><span class="sxs-lookup"><span data-stu-id="b25b7-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="b25b7-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b25b7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25b7-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="b25b7-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




