---
description: Generato da un'origine multimediale durante l'aggiornamento dei relativi metadati.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966804"
---
# <a name="mesourcemetadatachanged-event"></a>Evento MESourceMetadataChanged

Generato da un'origine multimediale durante l'aggiornamento dei relativi metadati.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Se l'origine del supporto non può fornire tutti i metadati quando l'origine viene creata per la prima volta, deve generare questo evento dopo che i metadati sono disponibili.

L'origine multimediale deve creare un nuovo descrittore di presentazione e copiare tutti gli attributi dal descrittore della presentazione (PD) nell'oggetto evento. L'applicazione può usare l'oggetto evento per enumerare i nuovi attributi PD. In particolare, i valori per le [ \_ \_ \_ \_ dimensioni del file](mf-pd-total-file-size-attribute.md) [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) e MF PD possono essere sconosciuti fino a quando il file non viene scaricato completamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




