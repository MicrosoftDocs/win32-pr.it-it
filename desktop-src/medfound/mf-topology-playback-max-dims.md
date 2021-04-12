---
description: Specifica le dimensioni della finestra di destinazione per la riproduzione video.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Attributo MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226630"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>\_ \_ \_ Attributo max Dim playback per la riproduzione della topologia \_

Specifica le dimensioni della finestra di destinazione per la riproduzione video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).

Per impostare questo attributo, chiamare [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Il caricatore della topologia usa questo attributo per ottimizzare la pipeline prima che venga avviata la riproduzione. Se si imposta questo attributo, impostare anche l'attributo di ottimizzazione per la [ \_ \_ \_ \_ riproduzione statica della topologia MF](mf-topology-static-playback-optimizations.md) su **true**.

I 32 bit superiori del valore dell'attributo contengono la larghezza e i 32 bit inferiori contengono l'altezza, in pixel.

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

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[Gestione della qualità dei video](video-quality-management.md)
</dt> </dl>

 

 




