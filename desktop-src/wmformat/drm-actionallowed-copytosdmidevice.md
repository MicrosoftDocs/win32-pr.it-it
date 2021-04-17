---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: L' \_ \_ attributo COPYTOSDMIDEVICE di DRM ActionAllowed indica se il contenuto può essere copiato in un dispositivo SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice formato Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398527"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="a18d2-104">\_CopyToSDMIDevice ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="a18d2-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="a18d2-105">L' **attributo \_ \_ CopyToSDMIDevice di DRM ActionAllowed** indica se il contenuto può essere copiato in un dispositivo SDMI.</span><span class="sxs-lookup"><span data-stu-id="a18d2-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a18d2-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a18d2-106">Global Constant</span></span>

<span data-ttu-id="a18d2-107">g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice</span><span class="sxs-lookup"><span data-stu-id="a18d2-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="a18d2-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a18d2-108">Data Type</span></span>

<span data-ttu-id="a18d2-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a18d2-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="a18d2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a18d2-110">Remarks</span></span>

<span data-ttu-id="a18d2-111">Licenze Windows Media DRM 10 usare l'azione di copia per limitare la copia ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a18d2-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="a18d2-112">Controllare la proprietà di [**\_ \_ copia DRM ActionAllowed**](drm-actionallowed-copy.md) per determinare se è consentita la copia.</span><span class="sxs-lookup"><span data-stu-id="a18d2-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="a18d2-113">Si tratta di una proprietà di sola lettura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="a18d2-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="a18d2-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a18d2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18d2-115">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="a18d2-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




