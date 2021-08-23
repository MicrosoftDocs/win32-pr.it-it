---
description: Specifica per una topologia di transcodifica se il caricatore della topologia carica le trasformazioni basate su hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e8715c135e074956af2280b8474172e94e69e1cca20cd01b020fc6dc79076c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663841"
---
# <a name="mf_transcode_topologymode-attribute"></a>Attributo MF \_ TRANSCODE \_ TOPOLOGYMODE

Specifica per una topologia di transcodifica se il caricatore della topologia carica le trasformazioni basate su hardware.

La modalità topologia specifica se è possibile usare trasformazioni hardware (ad esempio codec hardware) nella topologia di transcodifica. L'applicazione può archiviare questo attributo in un profilo transcodifica chiamando [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).

## <a name="data-type"></a>Tipo di dati

**[**MF \_ FLAG TRANSCODE \_ TOPOLOGYMODE \_ archiviati**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** **come UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Deve avere uno dei valori seguenti.



| Valore                                              | Descrizione                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HARDWARE MF \_ TRANSCODE \_ TOPOLOGYMODE \_ \_ CONSENTITO** | Il caricatore della topologia carica MFT basati su hardware, ad esempio decodificatori hardware, quando disponibile.<br/> Il caricatore della topologia esegue automaticamente il fall back alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.<br/> |
| **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**    | Il caricatore della topologia carica solo MFT software, inclusi i decodificatori software.                                                                                                                                                                                                    |



 

Il valore predefinito è **MF \_ TRANSCODE \_ TOPOLOGYMODE \_ SOFTWARE \_ ONLY**.

Se il caricatore della topologia inserisce un MFT hardware nella topologia, imposta l'attributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) nel nodo della topologia. Per verificare se è presente un MFT hardware, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.

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

[API transcodifica](transcode-api.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




