---
title: DRM_ActionAllowed_CopyToCD
description: L' \_ \_ attributo COPYTOCD di DRM ActionAllowed indica se il contenuto può essere copiato in un CD.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299441"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="5609f-104">\_CopyToCD ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="5609f-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="5609f-105">L' **attributo \_ \_ CopyToCD di DRM ActionAllowed** indica se il contenuto può essere copiato in un CD.</span><span class="sxs-lookup"><span data-stu-id="5609f-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5609f-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="5609f-106">Global Constant</span></span>

<span data-ttu-id="5609f-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD</span><span class="sxs-lookup"><span data-stu-id="5609f-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="5609f-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5609f-108">Data Type</span></span>

<span data-ttu-id="5609f-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5609f-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="5609f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5609f-110">Remarks</span></span>

<span data-ttu-id="5609f-111">Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia su CD.</span><span class="sxs-lookup"><span data-stu-id="5609f-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="5609f-112">Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.</span><span class="sxs-lookup"><span data-stu-id="5609f-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="5609f-113">Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="5609f-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="5609f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5609f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5609f-115">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="5609f-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




