---
description: Specifica se i metadati vengono scritti nel file transcodificato.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7874d7d8cc20bbf5222cd8fd2fa0ca938c0b597dbc42914ab809dad926968306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739423"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>Attributo MF \_ TRANSCODE \_ SKIP METADATA \_ \_ TRANSFER

Specifica se i metadati vengono scritti nel file transcodificato. Questo attributo del contenitore viene archiviato nel profilo di transcodifica.

## <a name="data-type"></a>Tipo di dati

**UINT32**

I valori possibili per l'attributo MF \_ TRANSCODE \_ SKIP METADATA TRANSFER sono descritti nella tabella \_ \_ seguente.



| Valore                                                                        | Significato                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Trasferisce automaticamente i metadati a livello di file dal file di origine al file transcodificato.<br/> |
| <dl> <dt>1</dt> </dl> | I metadati del file di origine non vengono scritti nel file transcodificato.<br/>                          |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




