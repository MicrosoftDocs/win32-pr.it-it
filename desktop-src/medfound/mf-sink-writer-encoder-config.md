---
description: Contiene un puntatore a un archivio di proprietà con proprietà di codifica.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Attributo MF_SINK_WRITER_ENCODER_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757400"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>\_Attributo di \_ \_ configurazione del codificatore MF sink writer \_

Contiene un puntatore a un archivio di proprietà con proprietà di codifica.

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Questo attributo consente a un'applicazione di impostare le proprietà di codifica quando si utilizza il [writer del sink](sink-writer.md). Per impostare questo attributo, seguire questa procedura:

1.  Chiamare [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un nuovo archivio delle proprietà.
2.  Impostare le proprietà del codificatore nell'archivio delle proprietà. Le proprietà disponibili dipendono dal codificatore. Per altre informazioni, vedere [oggetti codec](codecobjects.md).
3.  Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi.
4.  Chiamare [**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) per impostare il puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) nell'archivio di attributi.
5.  Crea una nuova istanza del writer del sink. Passare il puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) alla funzione di creazione. Per altre informazioni, vedere [sink writer Attributes](sink-writer-attributes.md).

Il writer di sink imposta le proprietà del codificatore prima di impostare i tipi di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> </dl>

 

 
