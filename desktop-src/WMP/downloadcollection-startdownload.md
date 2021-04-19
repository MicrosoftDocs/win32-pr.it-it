---
title: Metodo DownloadCollection. startDownload
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo startDownload Accoda un download.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- metodo startDownload Windows Media Player
- metodo startDownload Windows Media Player, classe DownloadCollection
- Scaricacollection (classe) Windows Media Player, metodo startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331485"
---
# <a name="downloadcollectionstartdownload-method"></a>Metodo DownloadCollection. startDownload

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **startDownload** Accoda un download.

## <a name="syntax"></a>Sintassi


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sourceURL* \[ in\]
</dt> <dd>

**Stringa** che specifica l'URL del download.

</dd> <dt>

*tipo* \[ di in\]
</dt> <dd>

**Stringa** che specifica il tipo di download. Contiene uno dei valori seguenti.



| Valore      | Descrizione                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP e versioni successive). Il download viene eseguito come processo in background, in quanto il tempo del processore diventa disponibile. Gli Stati di download vengono mantenuti anche quando Windows Media Player o Windows XP viene arrestato. |
| tempo reale  | (Tutti i sistemi operativi supportati). Il download viene eseguito in una sola volta. Nessun stato di download viene mantenuto tra le sessioni.                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **DownloadItem** .

## <a name="remarks"></a>Commenti

Quando viene avviato un nuovo download, gestione download lo aggiunge come elemento alla raccolta di download che ha avviato il download.

È possibile scaricare solo i formati multimediali digitali seguenti:

-   Advanced Systems Format (ASF)
-   MP3
-   Windows Media Audio (WMA)
-   Windows Media Video (WMV)

Il parametro *sourceURL* non supporta stringhe con codifica Unicode. Deve puntare al contenuto valido. I reindirizzamenti non sono supportati.

Quando si utilizza Windows XP, i file audio vengono inseriti automaticamente nelle sottocartelle **My Music** appropriate in base ai valori dei metadati a livello di file. I file video vengono inseriti nel \\ \\ \\  \\ *tipo* di numero casuale di download per musica, dove *numero casuale* è un valore casuale generato da Windows Media Player per ogni utente e il *tipo* è "tempo reale" o "sfondo", a seconda del tipo di download.

Quando si usa Windows Media Player 9 Series con Windows 98 e Windows Millennium Edition (me), i file audio e video vengono \\ inseriti nel \\ tipo di numero casuale di download Music \\  \\ , dove *numero casuale* è un valore casuale generato dal lettore per ogni utente e il *tipo* è "tempo reale" o "sfondo", a seconda del tipo di download.

Si noti che i file possono essere rinominati in base agli attributi dei metadati contenuti nel file e alle regole specificate dall'utente nella finestra di dialogo **Opzioni** . I file che non contengono metadati, ad esempio **album** o **Artist**, possono essere spostati in cartelle con etichetta Unknown Artist o Unknown album.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Download (oggetto)**](downloadcollection-object.md)
</dt> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





