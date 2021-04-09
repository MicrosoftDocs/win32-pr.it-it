---
description: Microsoft Windows fornisce alcune proprietà di sistema che è possibile utilizzare per i formati di file.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Proprietà di System-Defined per formati di file personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128518"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>Proprietà di System-Defined per formati di file personalizzati

Microsoft Windows fornisce alcune proprietà di sistema che è possibile utilizzare per i formati di file. Se si sta creando un formato di file personalizzato, è necessario supportare tutte le proprietà definite dal sistema come possibile. Prima di creare un gestore di proprietà personalizzato, è consigliabile esaminare i gestori forniti dal sistema per verificare se è possibile utilizzarne uno anziché scriverne di propri.

La tabella seguente classifica i formati di file e quindi elenca le proprietà di sistema più importanti che il formato di file deve supportare. Per garantire un'esperienza utente ottimale, è necessario supportare tutte le proprietà Priority 1 e 2 per la categoria del formato di file.

-   [Comunicazioni](#communications)
-   [Contatti](#contacts)
-   [Documents](#documents) (Documenti)
-   [Generico](#generic)
-   [Musica](#music)
-   [Immagini](#pictures)
-   [Video](#videos)
-   [Argomenti correlati](#related-topics)

## <a name="communications"></a>Comunicazioni



| Nome            | Proprietà                               | Priorità |
|-----------------|----------------------------------------|----------|
| Data di ricezione   | System. Message. DateReceived            | 1        |
| Da nomi      | System. Message. FromName                | 1        |
| Con allegati | System. Message. HasAttachments          | 1        |
| Mailbox         | System. Communication. storeddisplayname | 1        |
| Nome            | System. FileName                        | 1        |
| Oggetto         | System. Subject                         | 1        |
| Ai nomi        | System. Message. toName                  | 1        |
| Category        | System. Category                        | 2        |
| Tipo            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contatti



| Nome             | Proprietà                           | Priorità |
|------------------|------------------------------------|----------|
| Nome account     | System. Communication. AccountName   | 1        |
| Telefono ufficio   | System. Contact. BusinessTelephone   | 1        |
| Company          | System. Company                     | 1        |
| Indirizzo di posta elettronica    | System. Contact. PrimaryEmailAddress | 1        |
| Importanza       | System. ImportanceText              | 1        |
| Cellulare     | System. Contact. MobileTelephone     | 1        |
| Indirizzo aziendale | System. Contact. BusinessAddress     | 2        |
| Fax aziendale     | System. Contact. BusinessFaxNumber   | 2        |
| Category         | System. Category                    | 2        |
| Indirizzo abitazione     | System. Contact. HomeAddress         | 2        |
| Telefono abitazione       | System. Contact. HomeTelephone       | 2        |
| Titolo            | System.Title                       | 2        |



 

## <a name="documents"></a>Documenti



| Nome      | Proprietà             | Priorità |
|-----------|----------------------|----------|
| Autori   | System.Author        | 1        |
| Full-text | System. FullText      | 1        |
| Tag      | System.Keywords      | 1        |
| Tipo      | System.PerceivedType | 1        |
| Category  | System. Category      | 2        |
| Titolo     | System.Title         | 2        |



 

## <a name="generic"></a>Generico



| Nome     | Proprietà             | Priorità |
|----------|----------------------|----------|
| Autori  | System.Author        | 1        |
| Titolo    | System.Title         | 1        |
| Tipo     | System.PerceivedType | 1        |
| Category | System. Category      | 2        |
| Tag     | System.Keywords      | 2        |



 

## <a name="music"></a>Musica



| Nome         | Proprietà                     | Priorità |
|--------------|------------------------------|----------|
| \#           | System. Music. numero     | 1        |
| Album        | System. Music. AlbumTitle      | 1        |
| Gli artisti      | System. Music. Artist          | 1        |
| Genre        | System. Music. Genre           | 1        |
| Classificazione       | System. rating                | 1        |
| Titolo        | System.Title                 | 1        |
| Artista album | System. Music. AlbumArtist     | 2        |
| Velocità in bit     | System. audio. EncodingBitrate | 2        |
| Conduttori   | System. Music. Conductor       | 2        |
| Length       | System. Media. Duration        | 2        |
| Protetta    | System. DRM. protected       | 2        |
| Year         | System. Media. Year            | 2        |



 

## <a name="pictures"></a>Immagini



| Nome          | Proprietà                        | Priorità |
|---------------|---------------------------------|----------|
| Data importazione | System. DateImported             | 1        |
| Data di inizio    | System. Photo. DateTaken          | 1        |
| Classificazione        | System. rating                   | 1        |
| Tag          | System.Keywords                 | 1        |
| Tipo          | System.PerceivedType            | 1        |
| Autori       | System.Author                   | 2        |
| Produttore di fotocamere  | System. Photo. CameraManufacturer | 2        |
| Modello di fotocamera  | System. Photo. CameraModel        | 2        |
| Commenti      | System. Comment                  | 2        |
| Dimensioni    | System. image. Dimensions         | 2        |



 

## <a name="videos"></a>Video



| Nome         | Proprietà                 | Priorità |
|--------------|--------------------------|----------|
| Length       | System. Media. Duration    | 1        |
| Classificazione       | System. rating            | 1        |
| Tag         | System.Keywords          | 1        |
| Tipo         | System.PerceivedType     | 1        |
| Altezza frame | System. video. FrameHeight | 2        |
| Larghezza frame  | System. video. FrameWidth  | 2        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Sviluppo di gestori di proprietà per Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Sistema di proprietà](../properties/building-property-handlers.md)
</dt> <dt>

[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
