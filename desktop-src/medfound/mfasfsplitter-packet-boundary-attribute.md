---
description: Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0904c6b5a002d6aa18361365946a176521674ea22f7a45cc042b89d844c4210d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464061"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>Attributo MFASFSPLITTER \_ PACKET \_ BOUNDARY

Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se un buffer multimediale espone [**l'interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) tramite **QueryInterface** e il valore di questo attributo è diverso da zero, lo splitter ASF considera il buffer come l'inizio di un nuovo pacchetto.

Questo attributo si applica se si usa la barra di divisione ASF per analizzare i dati asf. Se i dati ASF hanno lunghezze di pacchetto variabili, è necessario impostare questo attributo nei buffer multimediali passati al metodo [**IMFASFSplitter::P arseData.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) Impostare l'attributo **su TRUE** se il buffer contiene l'inizio di un nuovo pacchetto. Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **FALSE**. I buffer non possono estendersi su più pacchetti.

Per i dati ASF con dimensioni fisse dei pacchetti, questo attributo non è obbligatorio e un buffer può estendersi su più pacchetti.

Si noti che le implementazioni standard di [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fornite da Media Foundation non espongono [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Per usare questo attributo, è necessario fornire la propria implementazione di **IMFMediaBuffer**. ad esempio, tramite il wrapping dei buffer restituiti da [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




