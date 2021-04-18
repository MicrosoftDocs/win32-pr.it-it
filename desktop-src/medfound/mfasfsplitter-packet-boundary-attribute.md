---
description: Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Attributo MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308419"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>\_Attributo limite del pacchetto MFASFSPLITTER \_

Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se un buffer multimediale espone l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) tramite **QueryInterface** e il valore di questo attributo è diverso da zero, il separatore ASF considera il buffer come l'inizio di un nuovo pacchetto.

Questo attributo si applica se si utilizza la barra di divisione ASF per analizzare i dati ASF. Se i dati ASF hanno lunghezze di pacchetti variabili, è necessario impostare questo attributo sui buffer multimediali passati al metodo [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Impostare l'attributo su **true** se il buffer contiene l'inizio di un nuovo pacchetto. Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **false**. I buffer non possono estendersi su più pacchetti.

Per i dati ASF con dimensioni di pacchetto fisse, questo attributo non è obbligatorio e un buffer può estendersi a più pacchetti.

Si noti che le implementazioni standard di [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fornite da Media Foundation non espongono [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Per usare questo attributo, è necessario fornire un'implementazione personalizzata di **IMFMediaBuffer**; ad esempio, eseguendo il wrapping dei buffer restituiti da [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




