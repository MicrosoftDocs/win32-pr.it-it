---
title: DRM_IsDRMCached
description: La \_ Proprietà DRM IsDRMCached indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached formato Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299447"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="d3c4f-104">\_ISDRMCACHED DRM</span><span class="sxs-lookup"><span data-stu-id="d3c4f-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="d3c4f-105">La proprietà **DRM \_ IsDRMCached** indica se le informazioni sulla licenza DRM versione 1 sono state archiviate nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d3c4f-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="d3c4f-106">Global Constant</span></span>

<span data-ttu-id="d3c4f-107">g \_ wszWMDRM \_ IsDRMCached</span><span class="sxs-lookup"><span data-stu-id="d3c4f-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="d3c4f-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d3c4f-108">Data Type</span></span>

<span data-ttu-id="d3c4f-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d3c4f-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c4f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3c4f-110">Remarks</span></span>

<span data-ttu-id="d3c4f-111">Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d3c4f-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="d3c4f-112">È **vero** quando l'URL di acquisizione della licenza corrisponde a uno dei due URL di conoscenza usati per l'acquisizione della licenza locale in DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="d3c4f-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3c4f-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3c4f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c4f-114">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="d3c4f-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




