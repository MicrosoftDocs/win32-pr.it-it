---
description: Contiene un puntatore a un archivio delle proprietà con proprietà di codifica.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb68348987ac406643cbe709dc6052d1add3c04e63b4e1f38d7c681a95c3ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059085"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>Attributo MF \_ SINK \_ WRITER ENCODER \_ \_ CONFIG

Contiene un puntatore a un archivio delle proprietà con proprietà di codifica.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un [**puntatore IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Questo attributo consente a un'applicazione di impostare le proprietà di codifica quando si usa il [writer di sink](sink-writer.md). Per impostare questo attributo, seguire questa procedura:

1.  Chiamare [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) per creare un nuovo archivio delle proprietà.
2.  Impostare le proprietà del codificatore nell'archivio delle proprietà. Le proprietà disponibili dipendono dal codificatore. Per altre informazioni, vedere [Oggetti codec.](codecobjects.md)
3.  Chiamare [**MFCreateAttributes per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) creare un nuovo archivio attributi.
4.  Chiamare [**IMFAttributes::SetUnknown per**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) impostare il [**puntatore IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) nell'archivio attributi.
5.  Creare una nuova istanza del writer di sink. Passare il [**puntatore IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) alla funzione di creazione. Per altre informazioni, vedere [Attributi del writer di sink.](sink-writer-attributes.md)

Il writer di sink imposta le proprietà nel codificatore prima di impostare i tipi di supporti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> </dl>

 

 
