---
description: Specifica le dimensioni della finestra di destinazione per la riproduzione video.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98575a32b1d68414cb4d94a547273aa4986e03dc707023d5c40f9860b77b5a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604781"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>Attributo MAX \_ \_ DIMS PER LA RIPRODUZIONE \_ \_ DELLA TOPOLOGIA MF

Specifica le dimensioni della finestra di destinazione per la riproduzione video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**MFGetAttributeSize.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)

Per impostare questo attributo, chiamare [**MFSetAttributeSize.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize)

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Il caricatore della topologia usa questo attributo per ottimizzare la pipeline prima dell'avvio della riproduzione. Se si imposta questo attributo, impostare anche l'attributo OTTIMIZZAZIONI RIPRODUZIONE [ \_ \_ STATICA \_ \_](mf-topology-static-playback-optimizations.md) DELLA TOPOLOGIA MF su **TRUE**.

I 32 bit superiori del valore dell'attributo contengono la larghezza e i 32 bit inferiori contengono l'altezza, entrambi in pixel.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

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

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[Gestione della qualità dei video](video-quality-management.md)
</dt> </dl>

 

 




