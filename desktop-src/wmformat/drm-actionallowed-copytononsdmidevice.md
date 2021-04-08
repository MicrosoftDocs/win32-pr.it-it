---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: L' \_ \_ attributo COPYTONONSDMIDEVICE di DRM ActionAllowed indica se il contenuto può essere copiato in un dispositivo non SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046336"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="f3d22-104">\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="f3d22-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="f3d22-105">L' **attributo \_ \_ CopyToNonSDMIDevice di DRM ActionAllowed** indica se il contenuto può essere copiato in un dispositivo non SDMI</span><span class="sxs-lookup"><span data-stu-id="f3d22-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="f3d22-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="f3d22-106">Global Constant</span></span>

<span data-ttu-id="f3d22-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="f3d22-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="f3d22-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f3d22-108">Data Type</span></span>

<span data-ttu-id="f3d22-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="f3d22-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="f3d22-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3d22-110">Remarks</span></span>

<span data-ttu-id="f3d22-111">Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f3d22-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="f3d22-112">Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.</span><span class="sxs-lookup"><span data-stu-id="f3d22-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="f3d22-113">Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="f3d22-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="f3d22-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3d22-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d22-115">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="f3d22-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




