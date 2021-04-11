---
description: Indica all'allocatore del video di esempio di creare trame condivisibili tramite mutex con chiave.
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: Attributo MF_SA_D3D11_SHARED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6ecb23a99a732e183bc16942e33bbb4f8e3a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231773"
---
# <a name="mf_sa_d3d11_shared-attribute"></a>\_ \_ Attributo condiviso MF SA d3d11 \_

Indica all'allocatore del video di esempio di creare trame condivisibili tramite mutex con chiave.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

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
</dt> <dt>

[**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[MF \_ sa \_ d3d11 \_ condiviso \_ senza \_ mutex](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




