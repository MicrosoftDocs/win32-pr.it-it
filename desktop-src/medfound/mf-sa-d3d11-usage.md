---
description: Specifica come allocare superfici Microsoft Direct3D 11 per campioni multimediali.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7364b9777d94baa1a6c25aead6631ad6b11dcddc12db83698da04affebe0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663951"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>Attributo MF \_ SA \_ D3D11 \_ USAGE

Specifica come allocare superfici Microsoft Direct3D 11 per campioni multimediali. L'utilizzo riflette direttamente se un campione è accessibile dalla CPU o dalla GPU.

## <a name="data-type"></a>Tipo di dati

**D3D11 \_ USAGE** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un [**valore D3D11 \_ USAGE.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation trasformazioni

In questo contesto, l'attributo si applica solo quando la trasformazione Microsoft Media Foundation (MFT) restituisce **TRUE** per l'attributo [MF \_ SA \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)

Se un MFT supporta Direct3D 11, questo attributo fornisce un hint a MFT durante l'allocazione delle superfici Microsoft Direct3D per l'output. Impostare l'attributo come segue:

1.  Chiamare [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) per ottenere l'archivio attributi MFT.
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La pipeline Media Foundation imposta l'attributo prima dell'avvio del flusso. Il MFT deve tentare di rispettare l'impostazione quando alloca le superfici. Se ciò non è possibile, il MFT può ignorare l'attributo, anziché non eseguire l'allocazione.

Inoltre, se la MFT richiede superfici Direct3D per l'input, può esporre questo attributo come suggerimento per la modalità di allocazione delle superfici di input. Eseguire una query sull'attributo come segue:

1.  Chiamare [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) per ottenere gli attributi del flusso di input.
2.  Chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Allocatore di esempio

Questo attributo può essere impostato nell'allocatore di esempio video, nel [**metodo IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
