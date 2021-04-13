---
description: Specifica se i metadati vengono scritti nel file transcodificato.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Attributo MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226373"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>\_Attributo per il \_ \_ trasferimento dei metadati con MF transcode Skip \_

Specifica se i metadati vengono scritti nel file transcodificato. Questo attributo del contenitore viene archiviato nel profilo transcodifica.

## <a name="data-type"></a>Tipo di dati

**UINT32**

\_ \_ \_ Nella tabella seguente sono descritti i valori possibili per l'attributo MF transcode Skip Metadata \_ transfer.



| Valore                                                                        | Significato                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Trasferisce automaticamente i metadati a livello di file dal file di origine al file transcodificato.<br/> |
| <dl> <dt>1</dt> </dl> | I metadati del file di origine non vengono scritti nel file transcodificato.<br/>                          |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

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

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




