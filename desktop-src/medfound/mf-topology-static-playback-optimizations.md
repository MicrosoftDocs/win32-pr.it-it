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
# <a name="mf_topology_static_playback_optimizations-attribute"></a>\_ \_ \_ Attributo ottimizzazione riproduzione statica topologia MF \_

Abilita le ottimizzazioni statiche nella pipeline video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Impostare questo attributo prima di caricare una topologia. Se l'attributo è **true**, il caricatore della topologia tenta di ottimizzare la pipeline prima che venga avviata la riproduzione.

Se si imposta questo attributo, è necessario impostare anche gli attributi seguenti:

-   [\_framerate di riproduzione della topologia MF \_ \_](mf-topology-playback-framerate.md)
-   [MF \_ \_ massima riproduzione topologia \_ \_ Dim](mf-topology-playback-max-dims.md)

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[Gestione della qualità dei video](video-quality-management.md)
</dt> </dl>

 

 




