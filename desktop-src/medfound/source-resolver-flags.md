---
description: Definisce il comportamento del resolver di origine. Questi flag vengono inoltre utilizzati dai gestori dello schema e dai gestori del flusso di byte.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Flag del resolver di origine (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31efe47f75151f78958903cb514653edb6c5aa08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753858"
---
# <a name="source-resolver-flags"></a>Flag del resolver di origine

Definisce il comportamento del resolver di origine. Questi flag vengono inoltre utilizzati dai gestori dello schema e dai gestori del flusso di byte.



| Costante/valore                                                                                                                                                                                                                                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ 0x00000001 \_ MEDIASOURCE risoluzione**</dt> <dt></dt> </dl>                                                                                                                                           | Tentativo di creare un'origine multimediale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ Risoluzione \_ BYTESTREAM**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Tentativo di creazione di un flusso di byte.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **\_ \_ Il contenuto di risoluzione MF non \_ \_ \_ deve necessariamente \_ \_ corrispondere all' \_ estensione o al \_ \_ \_ tipo MIME**</dt> <dt>0x00000010</dt> </dl> | Se la risoluzione dell'origine ha esito negativo utilizzando il gestore del flusso di byte registrato per il tipo MIME o l'estensione del nome di file, il resolver di origine enumera tutti i gestori del flusso di byte registrati.<br/> I gestori del flusso di byte sono registrati dall'estensione del nome file o dal tipo MIME. Inizialmente, il resolver di origine tenta di utilizzare un gestore che corrisponde all'estensione del nome file o al tipo MIME. Se l'operazione ha esito negativo, per impostazione predefinita l'intera risoluzione dell'origine ha esito negativo e il resolver di origine restituisce un codice di errore all'applicazione. Se questo flag è specificato, tuttavia, il resolver di origine continua a enumerare tutti i gestori del flusso di byte registrati. Probabilmente un gestore con corrispondenza errata può creare correttamente l'origine multimediale.<br/> Questo flag non può essere combinato con il \_ flag di conservazione del flusso di byte della risoluzione MF \_ \_ \_ \_ attivo \_ su \_ non riuscito. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ La \_ risoluzione \_ mantiene \_ \_ il flusso di byte attivo \_ in 0x00000020 \_ non riuscito**</dt> <dt></dt> </dl>                                                                             | Se la risoluzione dell'origine ha esito negativo, il resolver di origine non chiude il flusso di byte. Per impostazione predefinita, il resolver di origine chiude il flusso di byte in caso di errore.<br/> Se questo flag viene usato e la risoluzione dell'origine ha esito negativo, il chiamante deve chiamare nuovamente il metodo e impostare il contenuto della risoluzione MF non \_ \_ \_ \_ \_ deve \_ \_ corrispondere al flag di tipo di \_ estensione \_ o \_ MIME \_ .<br/> Questo flag non può essere combinato con il \_ contenuto di risoluzione MF non \_ \_ \_ \_ deve \_ \_ corrispondere al flag di \_ \_ tipo MIME o di estensione \_ \_ . Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ 0x00010000 di \_ lettura della risoluzione**</dt> <dt></dt> </dl>                                                                                                                                                                | Richiede l'accesso in lettura all'origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ 0x00020000 \_ scrittura risoluzione**</dt> <dt></dt> </dl>                                                                                                                                                             | Richiede l'accesso in scrittura all'origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ Risoluzione \_ disabilitare \_ i \_ plugin locali**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | Il resolver di origine non userà lo schema registrato localmente o i plug-in del gestore ByteStream.<br/> Richiede Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Commenti

L'applicazione imposta questi flag quando usa l'interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) . Il resolver di origine passa gli stessi flag ai metodi [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) e [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) .

È necessario specificare uno dei flag MF \_ Solution \_ MEDIASOURCE o MF \_ risoluzione \_ BYTESTREAM. I flag rimanenti sono tutti facoltativi.

Il \_ flag di \_ mantenimento del \_ flusso di byte per la risoluzione MF \_ \_ \_ in \_ caso di errore è definito per lo scenario seguente:

1.  L'applicazione tenta di aprire un'origine sulla rete. L'applicazione imposta il \_ \_ \_ flag di mantenimento del \_ flusso di byte di risoluzione MF \_ attivo \_ su \_ non riuscito.

2.  L'URL dell'origine contiene l'estensione del nome file non corretta. Poiché l'estensione del nome di file non è corretta, il gestore del flusso di byte predefinito non è in grado di creare l'origine multimediale. Dal momento che l'applicazione ha impostato il \_ \_ \_ flag di mantenimento del flusso di byte della risoluzione MF in stato \_ \_ \_ di \_ errore, il resolver di origine memorizza nella cache il flusso di byte.

3.  Il resolver di origine restituisce un codice di errore all'applicazione.

4.  Il client riapre l'origine, questa volta impostando il \_ contenuto della risoluzione MF non \_ \_ \_ \_ è necessario \_ che \_ corrisponda al \_ flag di \_ tipo MIME o di estensione \_ \_ . Questo flag fa in modo che il resolver di origine provi tutti i gestori registrati anziché solo il gestore predefinito. Poiché il flusso di byte è stato memorizzato nella cache, non è necessario che il resolver di origine Apra nuovamente il flusso di byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Media Foundation](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 




