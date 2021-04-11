---
title: Come funzionano i pacchetti di download di Windows Media (deprecato)
description: Come funzionano i pacchetti di download di Windows Media (deprecato)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, informazioni
- Pacchetti di download di Windows Media, funzionamento dei pacchetti
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116796"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Come funzionano i pacchetti di download di Windows Media (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Un pacchetto di download di Windows Media viene avviato da un sito Web quando un utente fa clic su un collegamento in un Web browser, ad esempio Microsoft Internet Explorer. Questa azione apre Windows Media Player, quindi Scarica e Annulla il pacchetto del pacchetto di download di Windows Media sul disco rigido dell'utente in una cartella predefinita.

Una volta estratti i file dal pacchetto di download di Windows Media, Windows Media Player individua una playlist Windows Media Metafile con estensione di file ASX tra i file in pacchetto. Se ne trova uno, il lettore crea una playlist basata sul metafile incluso. I file che contengono contenuto multimediale vengono quindi aggiunti alla libreria.

Windows Media Player cerca anche un elemento **Skin** nel metafile. Se l'elemento **Skin** contiene un riferimento a un file di bordo con estensione WMZ, il lettore carica il bordo nel riquadro **Now Playing** . Il lettore inizia quindi a riprodurre il contenuto fornito nel pacchetto.

Il diagramma seguente illustra il modo in cui il contenuto viene inserito in un pacchetto in un file di download di Windows Media, pubblicato in un sito Web, scaricato e riprodotto in un computer client con Windows Media Player.

![come ottenere e riprodurre un file di download di Windows Media.](images/wmd-image.png) Download di Windows Media

Nella tabella seguente vengono descritti i tre elementi che costituiscono un pacchetto di download di Windows Media.



| Elemento Package    | Funzione                                                                                                                                                                                                                                        | Estensioni di file                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Bordo             | Interfaccia utente fissa e personalizzata creata dal proprietario del contenuto per la visualizzazione, il collegamento e la riproduzione di tutti i supporti inclusi nel pacchetto di download di Windows Media. Le tecniche utilizzate per creare i bordi sono simili a quelle utilizzate per creare le interfacce. | wmz                                     |
| Playlist metafile  | Metafile di Windows Media contenente elementi **voce** , informazioni sulla playlist e un'identità dell'elemento **Skin** per i file di contenuto.                                                                                                             | .asx                                     |
| Contenuto multimediale | File contenente qualsiasi formato audio o video supportato da Windows Media Player.                                                                                                                                                          | WMA, WMV, ASF, WAV, AVI, MPG, MP3 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pacchetti di download di Windows Media (deprecato)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




