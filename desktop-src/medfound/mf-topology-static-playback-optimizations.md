---
description: Abilita le ottimizzazioni statiche nella pipeline video.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: Attributo MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318051"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="ac94a-103">\_ \_ \_ Attributo ottimizzazione riproduzione statica topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="ac94a-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="ac94a-104">Abilita le ottimizzazioni statiche nella pipeline video.</span><span class="sxs-lookup"><span data-stu-id="ac94a-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac94a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ac94a-105">Data type</span></span>

<span data-ttu-id="ac94a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac94a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ac94a-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ac94a-107">Get/set</span></span>

<span data-ttu-id="ac94a-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ac94a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ac94a-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ac94a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ac94a-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ac94a-110">Applies to</span></span>

[<span data-ttu-id="ac94a-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="ac94a-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="ac94a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac94a-112">Remarks</span></span>

<span data-ttu-id="ac94a-113">Impostare questo attributo prima di caricare una topologia.</span><span class="sxs-lookup"><span data-stu-id="ac94a-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="ac94a-114">Se l'attributo è **true**, il caricatore della topologia tenta di ottimizzare la pipeline prima che venga avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ac94a-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="ac94a-115">Se si imposta questo attributo, è necessario impostare anche gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac94a-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="ac94a-116">\_framerate di riproduzione della topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac94a-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="ac94a-117">MF \_ \_ massima riproduzione topologia \_ \_ Dim</span><span class="sxs-lookup"><span data-stu-id="ac94a-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="ac94a-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ac94a-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="ac94a-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="ac94a-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="ac94a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac94a-120">Requirements</span></span>



| <span data-ttu-id="ac94a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac94a-121">Requirement</span></span> | <span data-ttu-id="ac94a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ac94a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac94a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac94a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ac94a-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ac94a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac94a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac94a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ac94a-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac94a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac94a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac94a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac94a-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac94a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac94a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac94a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac94a-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac94a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac94a-131">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="ac94a-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac94a-132">Gestione della qualità dei video</span><span class="sxs-lookup"><span data-stu-id="ac94a-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




