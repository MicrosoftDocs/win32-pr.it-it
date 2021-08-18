---
description: Specifica il numero di buffer creati dall'allocatore video-sample per ogni campione video.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6b54cc5b2589649c954d9f2f41923af04fdf4aa7c00714067bee0b11dabbee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740368"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>MF \_ SA \_ BUFFERS PER ATTRIBUTO \_ \_ SAMPLE

Specifica il numero di buffer creati dall'allocatore video-sample per ogni campione video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Se si usa [**l'interfaccia IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare esempi video, è possibile usare questo attributo per creare esempi video che contengono più buffer. Ad esempio, se il valore dell'attributo è 2, l'allocatore crea due buffer video per ogni campione video. Impostare l'attributo nel *parametro pAttributes* del [**metodo IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

Il valore predefinito è 1. Se l'attributo non è impostato, l'allocatore crea esempi video che contengono un singolo buffer per campione.

Questo attributo è destinato principalmente alle trasformazioni Media Foundation (MFT) che supportano l'output 3D stereo, nella situazione seguente:

-   MFT supporta Microsoft DirectX Graphic Infrastructure (DXGI).
-   MFT alloca i propri esempi di output.
-   MFT usa [**l'interfaccia IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) per allocare gli esempi di output.
-   Il formato video 3D usa un buffer separato per ogni visualizzazione.

Se tutti questi criteri sono true, MFT deve impostare il valore dell'attributo su 2 (un buffer per ogni vista).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




