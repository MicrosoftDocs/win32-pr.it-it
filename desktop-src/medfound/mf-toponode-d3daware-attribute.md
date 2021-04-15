---
description: Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Attributo MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485812"
---
# <a name="mf_toponode_d3daware-attribute"></a>\_Attributo MF TOPONODE \_ D3DAWARE

Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).

Le applicazioni in genere non utilizzano direttamente questo attributo. La sessione multimediale imposta questo attributo su un nodo di trasformazione se la trasformazione Media Foundation sottostante dispone dell'attributo in grado di riconoscere la tecnologia [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




