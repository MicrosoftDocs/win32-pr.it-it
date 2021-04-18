---
description: Specifica se il caricatore della topologia Abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Attributo MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306754"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_ \_ Attributo modalità DXVA TOPOLOGIa MF \_

Specifica se il caricatore della topologia Abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.

## <a name="data-type"></a>Tipo di dati

**[**MFTOPOLOGY \_ \_Modalità DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** archiviata come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una costante di enumerazione della [**\_ \_ Modalità DXVA di MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . Il valore predefinito è **MFTOPOLOGY \_ DXVA \_ default**.

Questo attributo controlla quali MFTs ricevono un puntatore a gestione dispositivi Direct3D. Per abilitare l'accelerazione video completa, impostare il valore su **MFTOPOLOGY \_ DXVA \_ full**. Il valore **MFTOPOLOGY \_ DXVA \_ default** è definito per compatibilità con le versioni precedenti, ma corrisponde al comportamento di tutte le versioni precedenti di Microsoft Media Foundation.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestione dispositivi Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




