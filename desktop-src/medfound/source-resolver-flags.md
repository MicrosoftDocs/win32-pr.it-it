---
description: Definisce il comportamento del sistema di risoluzione di origine. Questi flag vengono usati anche dai gestori dello schema e dai gestori di flussi di byte.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Flag del resolver di origine (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847821"
---
# <a name="source-resolver-flags"></a>Flag del resolver di origine

Definisce il comportamento del sistema di risoluzione di origine. Questi flag vengono usati anche dai gestori dello schema e dai gestori di flussi di byte.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ RISOLUZIONE \_ DI MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Provare a creare un'origine multimediale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ RISOLUZIONE \_ DI BYTESTREAM**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Provare a creare un flusso di byte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **IL CONTENUTO DELLA RISOLUZIONE MF \_ NON DEVE CORRISPONDERE \_ \_ \_ \_ \_ \_ \_ ALL'ESTENSIONE \_ O \_ \_**</dt> AL TIPO MIME <dt>0X00000010</dt> </dl> | Se la risoluzione dell'origine non riesce usando il gestore del flusso di byte registrato per il tipo MIME o l'estensione di file, il sistema di risoluzione di origine esegue l'enumerazione tramite tutti i gestori di flussi di byte registrati.<br/> I gestori del flusso di byte vengono registrati in base all'estensione del nome file o al tipo MIME. Inizialmente, il sistema di risoluzione di origine tenta di usare un gestore che corrisponde all'estensione del nome file o al tipo MIME. Se l'operazione ha esito negativo, per impostazione predefinita l'intera risoluzione dell'origine ha esito negativo e il sistema di risoluzione dell'origine restituisce un codice di errore all'applicazione. Se questo flag viene specificato, tuttavia, il sistema di risoluzione di origine continua a enumerare tutti i gestori del flusso di byte registrati. È possibile che un gestore con corrispondenza errata possa creare correttamente l'origine multimediale.<br/> Questo flag non può essere combinato con il flag MF \_ RESOLUTION KEEP BYTE STREAM ALIVE ON \_ \_ \_ \_ \_ \_ FAIL. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ RISOLUZIONE \_ MANTENERE ATTIVO IL FLUSSO DI BYTE IN CASO DI \_ \_ \_ \_ \_ ERRORE**</dt> <dt>0X00000020</dt> </dl>                                                                             | Se la risoluzione dell'origine ha esito negativo, il sistema di risoluzione di origine non chiude il flusso di byte. Per impostazione predefinita, il sistema di risoluzione di origine chiude il flusso di byte in caso di errore.<br/> Se questo flag viene usato e la risoluzione dell'origine ha esito negativo, il chiamante deve chiamare nuovamente il metodo e impostare il flag MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION OR \_ MIME \_ \_ \_ \_ \_ \_ \_ \_ \_ TYPE.<br/> Questo flag non può essere combinato con il flag MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION OR \_ MIME \_ \_ \_ \_ \_ \_ \_ \_ \_ TYPE. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ RISOLUZIONE \_ DELLE**</dt> <dt>0X00010000</dt> </dl>                                                                                                                                                                | Richiede l'accesso in lettura all'origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ RISOLUZIONE \_ DEI PROBLEMI DI**</dt> <dt>0X00020000</dt> </dl>                                                                                                                                                             | Richiede l'accesso in scrittura all'origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ RISOLUZIONE \_ \_ DISABILITARE I \_ PLUG-IN**</dt> <dt>LOCALI 0X00000040</dt> </dl>                                                                                                           | Il sistema di risoluzione di origine non userà lo schema registrato localmente o i plug-in del gestore bytestream.<br/> Richiede Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Commenti

L'applicazione imposta questi flag quando usa [**l'interfaccia IMFSourceResolver.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) Il sistema di risoluzione di origine passa gli stessi flag ai metodi [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) e [**IMFSchemeHandler::BeginCreateObject.**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)

È necessario specificare uno dei flag MF \_ RESOLUTION \_ MEDIASOURCE o MF \_ RESOLUTION \_ BYTESTREAM. I flag rimanenti sono tutti facoltativi.

Il flag MF \_ RESOLUTION KEEP BYTE STREAM ALIVE ON FAIL è definito per lo scenario \_ \_ \_ \_ \_ \_ seguente:

1.  L'applicazione tenta di aprire un'origine in rete. L'applicazione imposta il flag MF \_ RESOLUTION KEEP BYTE STREAM ALIVE ON \_ \_ \_ \_ \_ \_ FAIL.

2.  L'URL dell'origine contiene l'estensione di file errata. Poiché l'estensione del nome file è errata, il gestore del flusso di byte predefinito non può creare l'origine multimediale. Poiché l'applicazione ha impostato il flag MF RESOLUTION KEEP BYTE STREAM ALIVE ON FAIL, il resolver di origine \_ memorizza nella cache il flusso di \_ \_ \_ \_ \_ \_ byte.

3.  Il sistema di risoluzione dell'origine restituisce un codice di errore all'applicazione.

4.  Il client apre nuovamente l'origine, questa volta impostando il flag MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION \_ OR MIME \_ TYPE \_ \_ \_ \_ \_ \_ \_ \_ . Questo flag fa sì che il sistema di risoluzione di origine eserciti tutti i gestori registrati anziché solo il gestore predefinito. Poiché il flusso di byte è stato memorizzato nella cache, il sistema di risoluzione di origine non deve aprire nuovamente il flusso di byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation costanti](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 




