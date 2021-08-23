---
description: Specifica la durata di un flusso di byte, in unità da 100 nanosecondi.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION attributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ba32b394fa776b5b70a5a649292ffa205132645b15c24a57591483c734b238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826731"
---
# <a name="mf_bytestream_duration-attribute"></a>Attributo \_ MF BYTESTREAM \_ DURATION

Specifica la durata di un flusso di byte, in unità da 100 nanosecondi.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Se l'oggetto che crea il flusso di byte può determinare la durata, può impostare questo attributo. In un flusso di rete, ad esempio, la durata potrebbe far parte della descrizione della sessione.

Per ottenere il valore dell'attributo, chiamare **QueryInterface** sul flusso di byte per ottenere un puntatore [**all'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                                                    |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




