---
description: Specifica i flag di associazione da usare per l'allocazione di superfici Microsoft Direct3D 11 per gli esempi di supporti.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65f0fbc607ccdc8f878e25109fcadfdf8956007d99909d9a21c0e668951106d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102464"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>Attributo \_ \_ BINDFLAGS MF SA D3D11 \_

Specifica i flag di associazione da usare per l'allocazione di superfici Microsoft Direct3D 11 per gli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un **OR** bit per bit di flag [**BIND \_ \_ FLAG D3D11.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation trasformazioni

In questo contesto, l'attributo si applica solo quando la trasformazione Microsoft Media Foundation (MFT) restituisce **TRUE** per l'attributo [MF \_ SA \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)

Se un MFT supporta Direct3D 11, questo attributo fornisce un hint all'MFT durante l'allocazione delle superfici Microsoft Direct3D per l'output. Impostare l'attributo come segue:

1.  Chiamare [**IMFTransform::GetOutputStreamAttributes per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) ottenere l'archivio attributi MFT.
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La Media Foundation pipeline imposta l'attributo prima dell'avvio del flusso. L'MFT deve tentare di rispettare l'impostazione quando alloca le superfici. Se ciò non è possibile, MFT può ignorare l'attributo, anziché non eseguire l'allocazione.

Inoltre, se MFT richiede superfici Direct3D per l'input, può esporre questo attributo come suggerimento per l'allocazione delle superfici di input. Eseguire una query sull'attributo come segue:

1.  Chiamare [**IMFTransform::GetInputStreamAttributes per**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) ottenere gli attributi del flusso di input.
2.  Chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Allocatore di esempio

Questo attributo può essere impostato nell'allocatore di esempio video, nel metodo [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
