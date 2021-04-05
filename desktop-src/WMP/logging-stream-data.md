---
title: Registrazione dei dati del flusso
description: Registrazione dei dati del flusso
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Playlist Windows Media Metafile, registrazione dei dati del flusso
- playlist, dati del flusso di registrazione
- playlist di metafile, dati del flusso di registrazione
- Playlist Windows Media Metafile, registrazione dati di flusso
- playlist, registrazione dei dati di flusso
- playlist di metafile, registrazione dei dati di flusso
- registrazione dei dati del flusso
- registrazione dati di flusso
- Media Player di Windows, registrazione dei dati del flusso
- Windows Media Player, registrazione dati di flusso
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116929"
---
# <a name="logging-stream-data"></a>Registrazione dei dati del flusso

Le informazioni registrate possono essere acquisite e usate per determinare il comportamento del visualizzatore, ad esempio la frequenza di visualizzazione di un flusso o se un utente specifico ha visualizzato un flusso e per quanto tempo la qualità.

Le informazioni di registrazione vengono inviate automaticamente al server da cui ha avuto origine la playlist. È inoltre possibile inviare le informazioni di registrazione a server aggiuntivi, inclusi i server Web utilizzati esclusivamente per la registrazione. A tale scopo, usare l'elemento **LogURL** , specificando un URL valido per l'attributo **href** . È possibile includere elementi **LogURL** come elementi figlio dell'elemento **ASX** e come elementi figlio dei singoli elementi di **immissione** . Quando la playlist viene aperta per la prima volta, le informazioni di registrazione vengono inviate al server di origine e a ogni URL specificato in **LogURL** Children dell'elemento **ASX** . Quindi, quando viene raggiunta ogni voce, le informazioni di registrazione specifiche di tale voce vengono inviate a ogni URL specificato in **LogURL** Children dell'elemento **entry** .

Windows Media Format SDK supporta l'elemento **LogURL** tramite l'interfaccia **IWMSReaderNetworkConfig** e i metodi seguenti:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Oltre alle informazioni registrate automaticamente, una playlist di metafile può registrare informazioni personalizzate mediante l'uso dell'elemento **param** . Per utilizzare l'elemento **param** in questo modo, impostare l'attributo **Name** su "log:" seguito da un nome di campo di log e da uno spazio dei nomi XML facoltativo separato dal nome del campo da altri due punti (":"). Ogni elemento dopo i due due punti viene considerato come uno spazio dei nomi, quindi il nome del campo non deve contenere i due punti.

Il campo di log specificato nell'attributo **Name** viene impostato sul valore dell'attributo **value** . Se il log non contiene ancora un campo con il nome specificato, verrà aggiunto.

**Codice di esempio**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




