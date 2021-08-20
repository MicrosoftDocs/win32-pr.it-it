---
title: Funzionamento Windows pacchetti di download multimediali (deprecati)
description: Funzionamento Windows pacchetti di download multimediali (deprecati)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Metafile multimediali, Windows pacchetti di download multimediali
- Windows Media Player,Windows pacchetti di download multimediali
- metafile, Windows pacchetti di download multimediali
- Windows Pacchetti di Windows multimediali
- Windows Pacchetti di download multimediali, informazioni
- Windows Pacchetti di download multimediale, funzionamento dei pacchetti
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b1af3cd89ec5d9b232872747d53504a2ad07ddc15e740dc19fc4cb37e9322ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338972"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Funzionamento Windows pacchetti di download multimediali (deprecati)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Un Windows di download multimediale viene avviato da un sito Web quando un utente fa clic su un collegamento in un Web browser, ad esempio Microsoft Internet Explorer. Questa azione apre Windows Media Player e quindi scarica e annulla il pacchetto Windows Media Download nel disco rigido dell'utente in una cartella predefinita.

Dopo aver estratto i file dal pacchetto di download multimediale Windows, Windows Media Player individua una playlist metafile di Windows Media con estensione asx tra i file in pacchetto. Se ne trova una, Il lettore crea una playlist basata sul metafile incluso. I file che contengono contenuto multimediale vengono quindi aggiunti alla libreria.

Windows Media Player cerca anche un **elemento SKIN** nel metafile. Se **l'elemento SKIN** contiene un riferimento a un file di bordo con estensione wmz, Player carica il bordo nel **riquadro In** riproduzione. Il lettore inizia quindi a riprodurre il contenuto fornito nel pacchetto.

Il diagramma seguente illustra come il contenuto viene inserito in un file di download multimediale Windows, pubblicato in un sito Web, scaricato e riprodotto in un computer client usando Windows Media Player.

![come viene ottenuto e riprodotto un file di download di Windows Media.](images/wmd-image.png) Windows Download multimediale

Nella tabella seguente vengono descritti i tre elementi che costituiscono un pacchetto Windows download multimediale.



| Elemento Package    | Funzione                                                                                                                                                                                                                                        | Estensioni dei nomi di file                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Bordo             | Un'interfaccia utente fissa e personalizzata creata dal proprietario del contenuto per la visualizzazione, il collegamento e la riproduzione di tutti i file multimediali presenti nel pacchetto Windows Media Download. Le tecniche usate per creare bordi sono simili a quelle usate per creare le skin. | wmz                                     |
| Metafile Playlist  | Oggetto Windows metafile multimediale che contiene **elementi ENTRY,** informazioni sulla playlist e un'identità **dell'elemento SKIN** per i file di contenuto.                                                                                                             | .asx                                     |
| Contenuto multimediale | File contenente qualsiasi formato audio o video supportato da Windows Media Player.                                                                                                                                                          | wma, wmv, asf, wav, .avi, .mpg, .mp3 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Pacchetti di download multimediali (deprecati)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




