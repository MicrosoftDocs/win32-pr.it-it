---
description: Specifica il numero di buffer creati dall'allocatore di campionamento video per ogni esempio video.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: Attributo MF_SA_BUFFERS_PER_SAMPLE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753175"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>\_Buffer SA MF \_ \_ per attributo di \_ esempio

Specifica il numero di buffer creati dall'allocatore di campionamento video per ogni esempio video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Se si usa l'interfaccia [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare esempi video, è possibile usare questo attributo per creare esempi video contenenti più buffer. Se, ad esempio, il valore dell'attributo è 2, l'allocatore crea due buffer video per ogni esempio video. Impostare l'attributo nel parametro *pAttributes* del metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

Il valore predefinito è 1. Se l'attributo non è impostato, l'allocatore crea esempi video contenenti un singolo buffer per campione.

Questo attributo è destinato principalmente alle trasformazioni di Media Foundation (MFTs) che supportano l'output 3D stereo, nella situazione seguente:

-   Il MFT supporta Microsoft DirectX Graphics Infrastructure (DXGI).
-   Il MFT alloca gli esempi di output.
-   Il MFT usa l'interfaccia [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare gli esempi di output.
-   Il formato video 3D utilizza un buffer separato per ogni visualizzazione.

Se tutti questi criteri sono true, la MFT deve impostare il valore dell'attributo su 2 (un buffer per ogni visualizzazione).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




