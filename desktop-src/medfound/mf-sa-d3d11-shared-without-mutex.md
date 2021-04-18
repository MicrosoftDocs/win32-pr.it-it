---
description: Indica all'allocatore del video di esempio di creare trame come condivisibili usando il meccanismo legacy.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Attributo MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308462"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a>MF \_ sa \_ d3d11 \_ condiviso \_ senza l' \_ attributo mutex

Indica all'allocatore del video di esempio di creare trame come condivisibili usando il meccanismo legacy.

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

[MF \_ sa \_ d3d11 \_ condiviso](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




