---
title: DRM_IndividualizedVersion
description: L' \_ attributo DRM IndividualizedVersion viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata richiesta per accedere al contenuto.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336441"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="10701-104">\_INDIVIDUALIZEDVERSION DRM</span><span class="sxs-lookup"><span data-stu-id="10701-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="10701-105">L'attributo **DRM \_ IndividualizedVersion** viene archiviato nell'intestazione DRM e contiene la versione minima individualizzata richiesta per accedere al contenuto.</span><span class="sxs-lookup"><span data-stu-id="10701-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="10701-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="10701-106">Global Constant</span></span>

<span data-ttu-id="10701-107">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="10701-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="10701-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="10701-108">Data Type</span></span>

<span data-ttu-id="10701-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="10701-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="10701-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="10701-110">Remarks</span></span>

<span data-ttu-id="10701-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="10701-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="10701-112">Può essere impostato usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="10701-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="10701-113">Lo stesso attributo file può essere recuperato usando [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span><span class="sxs-lookup"><span data-stu-id="10701-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="10701-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10701-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10701-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="10701-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




