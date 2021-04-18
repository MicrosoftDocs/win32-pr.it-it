---
description: Questo argomento descrive le novità di Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 per le diverse versioni di Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Miglioramenti di DXGI 1,6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522385"
---
# <a name="dxgi-16-improvements"></a>Miglioramenti di DXGI 1,6

Questo argomento descrive le novità di Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 per le diverse versioni di Windows 10.

## <a name="windows-10-october-2018-update"></a>Aggiornamento di Windows 10 (ottobre 2018)

Queste API sono state aggiunte per Windows 10, versione 1809 (10,0; Build 17763) &mdash; Nota anche come aggiornamento di Windows 10 ottobre 2018.

- Interfaccia [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) e relativi metodi.

## <a name="windows-10-april-2018-update"></a>Aggiornamento di Windows 10 (aprile 2018)

Queste API sono state aggiunte per Windows 10, versione 1803 (10,0; Build 17134) &mdash; Nota anche come aggiornamento di Windows 10 aprile 2018.

- Enumerazione [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) .
- Interfaccia [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) e relativi metodi.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Per Windows 10, versione 1709 (10,0; Build 16299) &mdash; Nota anche come Windows 10 Fall Creators Update &mdash; queste costanti sono state aggiunte all'enumerazione [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) . 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Per Windows 10, versione 1703 (10,0; Build 15063), &mdash; Nota anche come Windows 10 Creators Update, &mdash; è stata aggiunta la seguente funzionalità a Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 per poter rilevare le visualizzazioni HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Rilevamento HDR (High Dynamic Range)

Queste API sono state aggiunte per poter rilevare le visualizzazioni HDR.

- Struttura [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)
- Enumerazione [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)
- Enumerazione [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)
- Struttura [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)
- [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) (funzione)
- Interfaccia [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) e relativi metodi
- Interfaccia [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) e relativi metodi

Sono inoltre state aggiunte costanti all'enumerazione [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) per supportare tali API.

## <a name="related-topics"></a>Argomenti correlati
[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
