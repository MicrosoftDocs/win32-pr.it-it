---
title: Informazioni sui metadati
description: Informazioni sui metadati
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player,metadata
- metadati, informazioni
- metadati,attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcccda2af46e60e4bb0733d17e35e1a50d1fe923e9775fa6b10d2c06e3a972a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865361"
---
# <a name="about-the-metadata"></a>Informazioni sui metadati

Windows Media Player 10 o versioni successive tenta di sincronizzare gli attributi di metadati seguenti.



| Attributo player | Costante globale WMDM  | Descrizione                                                                                                 | Versione necessaria                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | Stringa con terminazione **Null** contenente il nome dell'artista principale per l'album.                         | Windows Media Player 11 o versione successiva. |
| Album            | g \_ wszWMDMAlbumTitle  | Stringa con terminazione **Null** contenente il titolo dell'album in cui è stato originariamente rilasciato il contenuto.  | Windows Media Player 11 o versione successiva. |
| Autore           | g \_ wszWMDMAuthor      | Stringa con terminazione **Null** contenente il nome dell'attore o dell'artista multimediale associato al contenuto.    | Windows Media Player 11 o versione successiva. |
| BuyNow           | g \_ wszWMDMBuyNow      | **Valore** booleano che indica se l'utente ha scelto di acquistare il contenuto.                                 | Windows Media Player 10 o versione successiva. |
| WM/Genre         | g \_ wszWMDMGenre       | Stringa con terminazione **Null** contenente il genere del contenuto.                                             | Windows Media Player 11 o versione successiva. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD** contenente il numero di volte in cui l'utente ha riprodotto il file multimediale digitale.                        | Windows Media Player 10 o versione successiva. |
| ReleaseDate      | g \_ wszWMDMYear        | Data della versione originale dell'elemento.                                                               | Windows Media Player 11 o versione successiva. |
| Titolo            | g \_ wszWMDMTitle       | Stringa con terminazione **Null contenente** il titolo.                                                            | Windows Media Player 11 o versione successiva. |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** contenente il numero di traccia dell'elemento nell'album in cui è stato originariamente rilasciato.         | Windows Media Player 11 o versione successiva. |
| UserRating       | g \_ wszWMDMUserRating  | **Valore DWORD** contenente un valore che rappresenta la classificazione a stella specificata dall'utente per il file multimediale digitale. | Windows Media Player 10 o versione successiva. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento accelerato dei metadati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




