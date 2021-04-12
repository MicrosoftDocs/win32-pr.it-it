---
title: Convenzione di processo di Windows Media Player BITS
description: Windows Media Player può scaricare e aggiungere automaticamente elementi multimediali digitali alla libreria se si usa Servizio trasferimento intelligente in background (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player Online Stores, Servizio trasferimento intelligente in background (BITS)
- archivi online, Servizio trasferimento intelligente in background (BITS)
- digitare 2 archivi online, Servizio trasferimento intelligente in background (BITS)
- Servizio trasferimento intelligente in background (BITS)
- BITS (Servizio trasferimento intelligente in background)
- Windows Media Player Online Stores, convenzione del processo BITS
- negozi online, convenzione del processo BITS
- tipi 2 negozi online, convenzione del processo BITS
- Convenzione del processo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223992"
---
# <a name="windows-media-player-bits-job-convention"></a>Convenzione di processo di Windows Media Player BITS

Windows Media Player può scaricare e aggiungere automaticamente elementi multimediali digitali alla libreria se si usa [servizio trasferimento intelligente in background (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal). Per sfruttare i vantaggi di questa funzionalità, è necessario aggiungere il processo alla coda di trasferimento BITS e chiamare **Metodo ibackgroundcopyjob:: FileDescription**, specificando una stringa di descrizione che utilizza il formato corretto.

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

## <a name="syntax"></a>Sintassi

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

Valore a 32 bit generato in modo casuale che Windows Media Player utilizza per identificare il servizio.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*
</dt> <dd>

Nome provider. Questo valore deve corrispondere a un nome di chiave di archivio online valido.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

Nome dell'artista principale per l'album.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*
</dt> <dd>

Titolo dell'album.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*Numero*
</dt> <dd>

Numero di traccia del CD.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Titolo*
</dt> <dd>

Titolo del contenuto.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Durata*
</dt> <dd>

Durata del contenuto.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Classificazione*
</dt> <dd>

Classificazione per il contenuto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando Windows Media Player 10 o versioni successive USA BITS per scaricare il contenuto, enumera i processi nella coda di trasferimento ed esamina la stringa di descrizione per ogni processo. Se la stringa di descrizione corrisponde alla convenzione prevista, Windows Media Player Scarica il contenuto.

È necessario aggiungere un solo file multimediale digitale per il download a ogni processo BITS.

Dopo aver avviato un processo BITS utilizzando questa convenzione, è necessario consentire a Windows Media Player di completare il processo. Windows Media Player rimuoverà anche il processo dalla coda BITS, sposterà il file scaricato nel percorso in cui è stata salvata la musica rippata e aggiungerà il file scaricato alla libreria.

Il parametro *ServiceID* deve contenere un valore diverso da zero a 32 bit. Per creare questo valore, è consigliabile usare la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

Il nome file specificato con il parametro *localName* di **Metodo ibackgroundcopyjob:: AddFile** deve avere un'estensione di file WMA, WMV, MP3 o ASF.

I parametri rimanenti sono progettati per contenere i valori dei metadati correlati al contenuto. È possibile recuperare questi valori dalla pagina Web del negozio online usando **DownloadItem. GetItemInfo**. È possibile recuperare la raccolta di download corretta chiamando **downloadmanager. Getdownloadcollection** e specificando *ServiceID* come parametro *CollectionId* .

Windows Media Player controlla periodicamente la coda BITS mentre il lettore è in esecuzione. Per assicurarsi che Windows Media Player controlli la coda BITS per i processi di download, è necessario creare un valore nella seguente sottochiave del registro di sistema:

**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Services**

Il valore deve essere creato nel modo seguente.



| Nome                | Tipo      | Descrizione                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | Specifica se Windows Media Player deve controllare la coda BITS per i processi di download. Se il valore è zero, il lettore non verificherà la coda BITS. Il lettore deve controllare la coda se il valore è diverso da zero. |



 

È possibile utilizzare la sintassi alternativa seguente per aggiungere processi BITS non completati da Windows Media Player, ma per i quali vengono semplicemente visualizzate le informazioni sullo stato:

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Quando si usa la sintassi precedente, è necessario scrivere il codice per completare il download dei bit, organizzare il contenuto nel computer dell'utente e aggiungere il contenuto alla libreria, se necessario.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem. getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager. getdownloadcollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Riferimento per negozi online di tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 