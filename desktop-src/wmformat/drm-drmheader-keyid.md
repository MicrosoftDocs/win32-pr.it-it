---
title: DRM_DRMHeader_KeyID
description: L' \_ attributo DRM DRMHeader \_ keyId contiene l'ID chiave per il file.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID formato Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336345"
---
# <a name="drm_drmheader_keyid"></a><span data-ttu-id="4bb6a-104">\_KeyId DRMHEADER \_ DRM</span><span class="sxs-lookup"><span data-stu-id="4bb6a-104">DRM\_DRMHeader\_KeyID</span></span>

<span data-ttu-id="4bb6a-105">L'attributo **DRM \_ DRMHeader \_ KEYID** contiene l'ID chiave per il file.</span><span class="sxs-lookup"><span data-stu-id="4bb6a-105">The **DRM\_DRMHeader\_KeyID** attribute contains the key ID for the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4bb6a-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="4bb6a-106">Global Constant</span></span>

<span data-ttu-id="4bb6a-107">g \_ wszWMDRM \_ DRMHeader \_ keyId</span><span class="sxs-lookup"><span data-stu-id="4bb6a-107">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="4bb6a-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4bb6a-108">Data Type</span></span>

<span data-ttu-id="4bb6a-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="4bb6a-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb6a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4bb6a-110">Remarks</span></span>

<span data-ttu-id="4bb6a-111">Questo attributo è presente solo con contenuto DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="4bb6a-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="4bb6a-112">Può essere recuperato con [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="4bb6a-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="4bb6a-113">Per impostare l'ID chiave nel file usando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) è necessario usare la proprietà [**DRM \_ keyId**](drm-keyid.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb6a-113">To set the key ID on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_KeyID**](drm-keyid.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bb6a-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bb6a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb6a-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="4bb6a-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




