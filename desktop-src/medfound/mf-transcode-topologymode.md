---
description: Specifica per una topologia transcodificata se il caricatore della topologia caricherà le trasformazioni basate su hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Attributo MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879814"
---
# <a name="mf_transcode_topologymode-attribute"></a>\_Attributo transcode \_ TOPOLOGYMODE MF

Specifica per una topologia transcodificata se il caricatore della topologia caricherà le trasformazioni basate su hardware.

La modalità topologia specifica se è possibile utilizzare le trasformazioni hardware (ad esempio, i codec hardware) nella topologia transcodifica. L'applicazione può archiviare questo attributo in un profilo transcode chiamando [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo di dati

**[**MF \_ Transcodificare i \_ \_ flag TOPOLOGYMODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** archiviati come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Deve avere uno dei valori seguenti.



| Valore                                              | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ transcode \_ TOPOLOGYMODE \_ hardware \_ consentito** | Il caricatore della topologia caricherà i MFTs basati su hardware, ad esempio i decodificatori hardware, quando disponibili.<br/> Il caricatore della topologia esegue automaticamente il fallback alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.<br/> |
| **MF \_ transcode \_ TOPOLOGYMODE \_ \_ solo software**    | Il caricatore della topologia caricherà solo MFTs software, inclusi i decodificatori software.                                                                                                                                                                                                    |



 

Il valore predefinito è **MF \_ transcode \_ TOPOLOGYMODE \_ \_ solo software**.

Se il caricatore della topologia inserisce una MFT hardware nella topologia, imposta l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nel nodo della topologia. Per verificare se è presente un hardware MFT, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.

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

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




