---
title: Registrazione dei dati del flusso
description: Registrazione dei dati del flusso
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows playlist metafile multimediali,registrazione dei dati di flusso
- playlist, registrazione dei dati di flusso
- playlist di metafile, registrazione dei dati del flusso
- Windows Playlist di metafile multimediali, registrazione dei dati di flusso
- playlist, registrazione dei dati di flusso
- playlist di metafile, registrazione dei dati di flusso
- registrazione dei dati del flusso
- registrazione dei dati di flusso
- Windows Media Player,registrazione dei dati del flusso
- Windows Media Player,trasmettere la registrazione dei dati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0a2ae6fe4b647e8a5c19fc6f30562973b3280f37cd3af3a1b9d9093771959de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118865"
---
# <a name="logging-stream-data"></a>Registrazione dei dati del flusso

Le informazioni registrate possono essere acquisite e usate per determinare il comportamento del visualizzatore, ad esempio la frequenza di visualizzazione di un flusso o se un utente specifico ha visualizzato un flusso e per quanto tempo è determinato dalla qualità.

Le informazioni di registrazione vengono inviate automaticamente al server da cui ha avuto origine la playlist. È anche possibile inviare informazioni di registrazione ad altri server, inclusi i server Web utilizzati esclusivamente per la registrazione. A tale scopo, usare **l'elemento LOGURL,** specificando un URL valido per **l'attributo HREF.** È possibile includere **gli elementi LOGURL** come elementi figlio dell'elemento **ASX** e come elementi figlio di **singoli elementi ENTRY.** Quando la playlist viene aperta per la prima volta, le informazioni di registrazione vengono inviate al server di origine e a ogni URL specificato negli elementi figlio **LOGURL** **dell'elemento ASX.** Quando viene raggiunta ogni voce, le informazioni di registrazione specifiche di tale voce vengono quindi inviate a ogni URL specificato negli elementi figlio **LOGURL** **dell'elemento ENTRY.**

L Windows Media Format SDK supporta **l'elemento LOGURL** tramite l'interfaccia **IWMSReaderNetworkConfig** e i metodi seguenti:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Oltre alle informazioni registrate automaticamente, una playlist di metafile può registrare informazioni personalizzate tramite l'uso **dell'elemento PARAM.** Per usare l'elemento **PARAM** in questo modo, impostare l'attributo **NAME** su "log:" seguito da un nome di campo del log e da uno spazio dei nomi XML facoltativo separato dal nome del campo da altri due punti (":"). Tutti gli elementi dopo i secondi due punti vengono considerati come spazio dei nomi, quindi il nome del campo non deve contenere due punti.

Il campo del log specificato **nell'attributo NAME** viene impostato sul valore dell'attributo **VALUE.** Se il log non contiene già un campo con il nome specificato, verrà aggiunto.

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

[**Playlist metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento su elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




