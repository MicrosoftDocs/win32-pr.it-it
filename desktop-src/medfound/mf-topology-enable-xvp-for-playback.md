---
description: Specifica se il caricatore della topologia Abilita il processore del video transcodificato (XVP). per le conversioni, abilitazione della conversione di colori con accelerazione hardware.
title: Attributo MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321590"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>\_ \_ Abilita \_ XVP per la topologia MF \_ per l' \_ attributo playback

Specifica se il caricatore della topologia Abilita il processore del video transcodificato (XVP). per le conversioni, abilitazione della conversione di colori con accelerazione hardware.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Se questo attributo è impostato, il caricatore della topologia effettuerà il pull del processore video, se necessario, durante la risoluzione della topologia non transcodifica. Quando si utilizza la topologia per creare un [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) personalizzato, questo attributo indica al caricatore di usare XVP per le conversioni anziché il convertitore di colori legacy, abilitando così la conversione dei colori accelerata hardware; il convertitore di colori legacy è solo software.

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

 

 




