---
description: Specifica se il caricatore della topologia abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875732"
---
# <a name="mf_topology_dxva_mode-attribute"></a>Attributo MF \_ TOPOLOGY \_ DXVA \_ MODE

Specifica se il caricatore della topologia abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.

## <a name="data-type"></a>Tipo di dati

**[**MFTOPOLOGY \_ MODALITÀ DXVA \_**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** archiviata come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una [**costante di enumerazione MFTOPOLOGY \_ DXVA \_ MODE.**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) Il valore predefinito è **MFTOPOLOGY \_ DXVA \_ DEFAULT.**

Questo attributo controlla quali MFT ricevono un puntatore a Gestione dispositivi Direct3D. Per abilitare l'accelerazione video completa, impostare il valore su **MFTOPOLOGY \_ DXVA \_ FULL**. Il valore **MFTOPOLOGY \_ DXVA \_ DEFAULT** è definito per la compatibilità con le versioni precedenti. Corrisponde al comportamento di tutte le versioni precedenti di Microsoft Media Foundation.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestione dispositivi Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




