---
description: Indica all'allocatore di esempio video di creare trame condivisibili usando il meccanismo legacy.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: MF_SA_D3D11_SHARED_WITHOUT_MUTEX attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8495d0c2033f6ffbc1a212c9768af3157697eb588c968cb3fbd62959fa3515f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740303"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a>Attributo MF \_ SA \_ D3D11 \_ SHARED WITHOUT \_ \_ MUTEX

Indica all'allocatore di esempio video di creare trame condivisibili usando il meccanismo legacy.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

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
</dt> <dt>

[**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[MF \_ SA \_ D3D11 \_ CONDIVISO](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




