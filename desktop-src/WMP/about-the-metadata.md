---
title: Informazioni sui metadati
description: Informazioni sui metadati
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Media Player di Windows, metadati
- metadati, informazioni
- metadati, attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328519"
---
# <a name="about-the-metadata"></a>Informazioni sui metadati

Windows Media Player 10 o versioni successive tenta di sincronizzare i seguenti attributi di metadati.



| Attributo Player | Costante globale WMDM  | Descrizione                                                                                                 | Versione necessaria                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | **Stringa** con terminazione null che contiene il nome dell'artista principale per l'album.                         | Windows Media Player 11 o versione successiva. |
| Album            | g \_ wszWMDMAlbumTitle  | **Stringa** con terminazione null contenente il titolo dell'album in cui è stato rilasciato originariamente il contenuto.  | Windows Media Player 11 o versione successiva. |
| Autore           | g \_ wszWMDMAuthor      | **Stringa** con terminazione null che contiene il nome dell'autore o dell'attore multimediale associato al contenuto.    | Windows Media Player 11 o versione successiva. |
| CompraOra           | g \_ wszWMDMBuyNow      | **Valore booleano** che indica se l'utente ha scelto di acquistare il contenuto.                                 | Windows Media Player 10 o versione successiva. |
| WM/genre         | g \_ wszWMDMGenre       | **Stringa** con terminazione null contenente il genere del contenuto.                                             | Windows Media Player 11 o versione successiva. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD** contenente il numero di volte in cui l'utente ha eseguito il file multimediale digitale.                        | Windows Media Player 10 o versione successiva. |
| ReleaseDate      | g \_ wszWMDMYear        | Data della versione originale dell'elemento.                                                               | Windows Media Player 11 o versione successiva. |
| Titolo            | g \_ wszWMDMTitle       | **Stringa** con terminazione null che contiene il titolo.                                                            | Windows Media Player 11 o versione successiva. |
| WM/numero   | g \_ wszWMDMTrack       | **DWORD** contenente il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.         | Windows Media Player 11 o versione successiva. |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** contenente un valore che rappresenta la classificazione a stelle specificata dall'utente per il file multimediale digitale. | Windows Media Player 10 o versione successiva. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni del dispositivo per il trasferimento di metadati accelerati**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




