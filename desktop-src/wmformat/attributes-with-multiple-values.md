---
title: Attributi con più valori (Windows Media Format 11 SDK)
description: Attributi con più valori
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, più valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047708"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Attributi con più valori (Windows Media Format 11 SDK)

Alcuni degli attributi predefiniti possono avere più valori assegnati. Ad esempio, **Artist** è un attributo che può avere più valori. È possibile chiamare [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) più volte per aggiungere tutti i valori degli **artisti** necessari. Se si eseguono più chiamate a **AddAttribute** per gli attributi che non supportano più valori, il metodo può restituire un codice di errore o semplicemente ignorare la richiesta.

Nella tabella seguente sono elencati gli attributi che supportano più valori. Alcuni attributi possono avere più valori solo nei file ASF, mentre altri possono avere più valori sia nei file ASF che in quelli MP3.



| Attributo                                                 | Supporto per più valori |
|-----------------------------------------------------------|-----------------------------|
| [**Autore**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/categoria**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/conduttore**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/genre**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/lingua**](wm-language.md)                        | ASF, MP3                    |
| [**WM/lyrics \_ sincronizzati**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/umore**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/immagine**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 




