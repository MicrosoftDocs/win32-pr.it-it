---
title: Attributi con più valori (Windows Media Format 11 SDK)
description: Informazioni sugli attributi con più valori in Windows Media Format 11 SDK. Alcuni attributi degli elementi multimediali possono avere più valori.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK,attributi
- Advanced Systems Format (ASF), attributi
- ASF (Advanced Systems Format),attributi
- attributi, più valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262693"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Attributi con più valori (Windows Media Format 11 SDK)

Ad alcuni attributi predefiniti possono essere assegnati più valori. Ad esempio, **Artista** è un attributo che può avere più valori. È possibile chiamare [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) più volte per aggiungere tutti i valori **di Artista** necessari. Se si effettuano più chiamate ad **AddAttribute** per attributi che non supportano più valori, il metodo può restituire un codice di errore o semplicemente ignorare la richiesta.

Nella tabella seguente sono elencati gli attributi che supportano più valori. Alcuni attributi possono avere più valori solo nei file ASF, mentre altri possono avere più valori nei file ASF e MP3.



| Attributo                                                 | Supporto per più valori |
|-----------------------------------------------------------|-----------------------------|
| [**Autore**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Category**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/Sistema di controllo**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/Genre**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/Language**](wm-language.md)                        | ASF, MP3                    |
| [**WM/Lyrics \_ Synchronised**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/Wm/Wm**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Picture**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> </dl>

 

 




