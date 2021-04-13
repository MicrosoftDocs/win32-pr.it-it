---
description: Specifica la modalità di allocazione delle superfici Microsoft Direct3D 11 per gli esempi di supporti.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: Attributo MF_SA_D3D11_USAGE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226379"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>\_Attributo utilizzo di MF SA \_ d3d11 \_

Specifica la modalità di allocazione delle superfici Microsoft Direct3D 11 per gli esempi di supporti. L'utilizzo indica direttamente se un campione è accessibile dalla CPU o dalla GPU.

## <a name="data-type"></a>Tipo di dati

**D3d11 \_ UTILIZZO** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un valore di [**\_ utilizzo di d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

### <a name="microsoft-media-foundation-transforms"></a>Trasformazioni Microsoft Media Foundation

In questo contesto, l'attributo si applica solo quando la trasformazione Microsoft Media Foundation (MFT) restituisce **true** per l'attributo d3d11 in grado di [ \_ \_ \_ riconoscere il valore MF SA](mf-sa-d3d11-aware.md) .

Se una MFT supporta Direct3D 11, questo attributo fornisce un suggerimento alla MFT durante l'allocazione delle superfici di Microsoft Direct3D per l'output. Impostare l'attributo nel modo seguente:

1.  Chiamare [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) per ottenere l'archivio di attributi MFT.
2.  Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La pipeline Media Foundation imposta l'attributo prima dell'avvio del flusso. Il MFT deve tentare di rispettare l'impostazione quando alloca superfici. Se ciò non è possibile, il MFT può ignorare l'attributo, anziché l'allocazione.

Inoltre, se il MFT richiede l'input di superfici Direct3D, può esporre questo attributo come hint per la modalità di allocazione delle superfici di input. Eseguire una query sull'attributo come indicato di seguito:

1.  Chiamare [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) per ottenere gli attributi del flusso di input.
2.  Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Allocatore di esempio

Questo attributo può essere impostato nell'allocatore video di esempio, nel metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

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

 

 
