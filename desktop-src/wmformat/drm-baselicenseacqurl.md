---
title: DRM_BaseLicenseAcqURL
description: L' \_ attributo BaseLicenseAcqURL di DRM contiene un URL di base parziale a cui un'applicazione del lettore deve passare per ottenere una licenza per il contenuto.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL formato Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117355"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="5ec23-104">\_BASELICENSEACQURL DRM</span><span class="sxs-lookup"><span data-stu-id="5ec23-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="5ec23-105">L' **attributo \_ BaseLicenseAcqURL di DRM** contiene un URL di base parziale a cui un'applicazione del lettore deve passare per ottenere una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5ec23-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5ec23-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="5ec23-106">Global Constant</span></span>

<span data-ttu-id="5ec23-107">g \_ wszWMDRM \_ BaseLicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="5ec23-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="5ec23-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5ec23-108">Data Type</span></span>

<span data-ttu-id="5ec23-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="5ec23-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec23-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ec23-110">Remarks</span></span>

<span data-ttu-id="5ec23-111">Si tratta di una proprietà di lettura/scrittura facoltativa impostata e recuperata tramite [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="5ec23-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="5ec23-112">Viene fornito per consentire ai sistemi di distribuzione delle licenze di usare percorsi relativi nelle proprietà dell'URL di acquisizione delle licenze.</span><span class="sxs-lookup"><span data-stu-id="5ec23-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="5ec23-113">Dopo aver impostato questa proprietà, tutti gli URL di acquisizione delle licenze parziali nelle intestazioni di contenuto avranno l'URL di base aggiunto all'inizio dell'URL parziale per formare un URL completo per l'applicazione del lettore a cui passare.</span><span class="sxs-lookup"><span data-stu-id="5ec23-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="5ec23-114">La chiamata di **IWMDRMReader:: GetDRMProperty** per **DRM \_ BaseLicenseAcqURL** funzionerà solo nella stessa sessione in cui è stata impostata.</span><span class="sxs-lookup"><span data-stu-id="5ec23-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="5ec23-115">La proprietà non è archiviata nell'intestazione del contenuto; è dinamico e solo l'URL relativo viene archiviato nel contenuto.</span><span class="sxs-lookup"><span data-stu-id="5ec23-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ec23-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ec23-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec23-117">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="5ec23-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




