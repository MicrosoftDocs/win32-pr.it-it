---
description: Specifica se il caricatore della topologia abilita il processore video transcodifica (XVP). per le conversioni, abilitando la conversione dei colori con accelerazione hardware.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK attributo (Mfidl.h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875733"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>Attributo MF \_ TOPOLOGY \_ ENABLE \_ XVP \_ FOR \_ PLAYBACK

Specifica se il caricatore della topologia abilita il processore video transcodifica (XVP). per le conversioni, abilitando la conversione dei colori con accelerazione hardware.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Se questo attributo è impostato, il caricatore della topologia estrae il processore video, se necessario, durante la risoluzione della topologia non transcodifica. Quando si usa la topologia per creare una [propria topologia IMFTopology,](/windows/win32/api/mfidl/nn-mfidl-imftopology) questo attributo indica al caricatore di usare XVP per le conversioni anziché il convertitore di colori legacy, abilitando così la conversione dei colori con accelerazione hardware. Il convertitore di colori legacy è solo software.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestione dispositivi Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




