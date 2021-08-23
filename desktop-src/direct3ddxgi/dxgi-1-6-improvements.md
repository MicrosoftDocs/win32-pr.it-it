---
description: Questo argomento descrive le novità di Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 per varie versioni di Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Miglioramenti di DXGI 1.6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 748878cc041b0987a013608556cd9ec30aaf638e0fcac1ef9386a4675f57ef0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727581"
---
# <a name="dxgi-16-improvements"></a>Miglioramenti di DXGI 1.6

Questo argomento descrive le novità di Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 per varie versioni di Windows 10.

## <a name="windows-10-october-2018-update"></a>Aggiornamento di Windows 10 (ottobre 2018)

Queste API sono state aggiunte per Windows 10, versione 1809 (10.0; Build 17763) &mdash; nota anche come Aggiornamento di Windows 10 (ottobre 2018).

- [**Interfaccia IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) e relativi metodi.

## <a name="windows-10-april-2018-update"></a>Aggiornamento di Windows 10 (aprile 2018)

Queste API sono state aggiunte per Windows 10 versione 1803 (10.0; Build 17134) nota anche come aggiornamento &mdash; Windows 10 aprile 2018.

- [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) enumerazione.
- [**Interfaccia IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) e relativi metodi.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Ad Windows 10 versione 1709 (10.0; Build 16299) nota anche come Windows 10 Fall Creators Update queste costanti sono state aggiunte &mdash; &mdash; [**all'DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) di compilazione. 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Ad Windows 10 versione 1703 (10.0; Build 15063) nota anche come Windows 10 Creators Update la funzionalità seguente è stata aggiunta &mdash; a &mdash; Microsoft DirectX Graphic Infrastructure (DXGI) 1.6 per rilevare gli schermi HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Rilevamento hdr (High Dynamic Range)

Queste API sono state aggiunte per rilevare gli schermi HDR.

- [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3) struttura
- [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) enumerazione
- [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags) enumerazione
- [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) struttura
- [**Funzione DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)
- [**Interfaccia IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) e relativi metodi
- [**Interfaccia IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) e relativi metodi

Inoltre, sono state aggiunte costanti [**all'enumerazione DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) per supportare queste API.

## <a name="related-topics"></a>Argomenti correlati
[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
