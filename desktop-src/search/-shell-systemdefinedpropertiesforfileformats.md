---
description: Microsoft Windows fornisce una serie di proprietà di sistema che è possibile usare per i formati di file.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined proprietà per i formati di file personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28dcf137d10fffb3cc192acf66b1279b83fd079b6b81cf963dfed8a78408388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944501"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>System-Defined proprietà per i formati di file personalizzati

Microsoft Windows fornisce una serie di proprietà di sistema che è possibile usare per i formati di file. Se si crea un formato di file personalizzato, è necessario supportare il maggior numero possibile di proprietà definite dal sistema. Prima di creare un gestore di proprietà personalizzato, è necessario esaminare i gestori forniti dal sistema per verificare se è possibile usarne uno invece di scriverne uno personalizzato.

La tabella seguente classifica i formati di file e quindi elenca le proprietà di sistema più importanti che il formato di file deve supportare. Per offrire un'esperienza utente ottimale, è necessario supportare tutte le proprietà con priorità 1 e 2 per la categoria del formato di file.

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
| Data di ricezione   | System.Message.DateReceived            | 1        |
| Da nomi      | System.Message.FromName                | 1        |
| Ha allegati | System.Message.HasAttachments          | 1        |
| Mailbox         | System.Communication.storeddisplayname | 1        |
| Nome            | System.FileName                        | 1        |
| Oggetto         | System.Subject                         | 1        |
| Ai nomi        | System.Message.ToName                  | 1        |
| Category        | System.Category                        | 2        |
| Tipo            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Contatti



| Nome             | Proprietà                           | Priorità |
|------------------|------------------------------------|----------|
| Nome account     | System.Communication.AccountName   | 1        |
| Telefono ufficio   | System.Contact.BusinessTelephone   | 1        |
| Company          | System.Company                     | 1        |
| Indirizzo di posta elettronica    | System.Contact.PrimaryEmailAddress | 1        |
| Importanza       | System.ImportanceText              | 1        |
| Cellulare     | System.Contact.MobileTelephone     | 1        |
| Indirizzo aziendale | System.Contact.BusinessAddress     | 2        |
| Fax aziendale     | System.Contact.BusinessFaxNumber   | 2        |
| Category         | System.Category                    | 2        |
| Indirizzo della home page     | System.Contact.HomeAddress         | 2        |
| Telefono abitazione       | System.Contact.HomeTelephone       | 2        |
| Titolo            | System.Title                       | 2        |



 

## <a name="documents"></a>Documenti



| Nome      | Proprietà             | Priorità |
|-----------|----------------------|----------|
| Autori   | System.Author        | 1        |
| Full-text | System.FullText      | 1        |
| Tag      | System.Keywords      | 1        |
| Tipo      | System.PerceivedType | 1        |
| Category  | System.Category      | 2        |
| Titolo     | System.Title         | 2        |



 

## <a name="generic"></a>Generico



| Nome     | Proprietà             | Priorità |
|----------|----------------------|----------|
| Autori  | System.Author        | 1        |
| Titolo    | System.Title         | 1        |
| Tipo     | System.PerceivedType | 1        |
| Category | System.Category      | 2        |
| Tag     | System.Keywords      | 2        |



 

## <a name="music"></a>Musica



| Nome         | Proprietà                     | Priorità |
|--------------|------------------------------|----------|
| \#           | Sistema. Musica. TrackNumber     | 1        |
| Album        | Sistema. Musica. AlbumTitle      | 1        |
| Artisti      | Sistema. Musica. Artista          | 1        |
| Genre        | Sistema. Musica. Genere           | 1        |
| Classificazione       | System.Rating                | 1        |
| Titolo        | System.Title                 | 1        |
| Album Artist | Sistema. Musica. AlbumArtist     | 2        |
| Velocità in bit     | System.Audio.EncodingBitrate | 2        |
| Conduttori   | Sistema. Musica. Conduttore       | 2        |
| Length       | System.Media.Duration        | 2        |
| Protetta    | System.DRM.IsProtected       | 2        |
| Year         | System.Media.Year            | 2        |



 

## <a name="pictures"></a>Immagini



| Nome          | Proprietà                        | Priorità |
|---------------|---------------------------------|----------|
| Data importazione | System.DateImported             | 1        |
| Data di inizio    | System.Photo.DateTaken          | 1        |
| Classificazione        | System.Rating                   | 1        |
| Tag          | System.Keywords                 | 1        |
| Tipo          | System.PerceivedType            | 1        |
| Autori       | System.Author                   | 2        |
| Autore della fotocamera  | System.Photo.CameraManufacturer | 2        |
| Modello di fotocamera  | System.Photo.CameraModel        | 2        |
| Commenti      | System.Comment                  | 2        |
| Dimensioni    | System.Image.Dimensions         | 2        |



 

## <a name="videos"></a>Video



| Nome         | Proprietà                 | Priorità |
|--------------|--------------------------|----------|
| Length       | System.Media.Duration    | 1        |
| Classificazione       | System.Rating            | 1        |
| Tag         | System.Keywords          | 1        |
| Tipo         | System.PerceivedType     | 1        |
| Altezza frame | System.Video.FrameHeight | 2        |
| Larghezza frame  | System.Video.FrameWidth  | 2        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Sviluppo di gestori di proprietà per Windows ricerca](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Sistema di proprietà](../properties/building-property-handlers.md)
</dt> <dt>

[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
