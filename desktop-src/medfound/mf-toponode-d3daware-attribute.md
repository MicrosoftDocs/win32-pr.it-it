---
description: Specifica se la trasformazione associata a un nodo della topologia supporta DirectX Video Acceleration (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e49735a1178cc521efd152f4fa11ab7c84069b07d0e5001f0f0e8e38bec940ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607151"
---
# <a name="mf_toponode_d3daware-attribute"></a>Attributo MF \_ TOPONODE \_ D3DAWARE

Specifica se la trasformazione associata a un nodo della topologia supporta DirectX Video Acceleration (DXVA).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Le applicazioni in genere non usano questo attributo direttamente. La sessione multimediale imposta questo attributo in un nodo di trasformazione se la trasformazione Media Foundation ha l'attributo [**MF \_ SA \_ D3D \_ AWARE.**](mf-sa-d3d-aware-attribute.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




