---
title: Linee guida sull'estensione metafile
description: Linee guida sull'estensione metafile
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Metafile di Windows Media, estensioni
- Metafile di Windows Media, estensioni di file
- Metafile, estensioni
- Metafile, estensioni di file
- Windows Media, metafile
- estensioni dei nomi di file per i file multimediali di Windows
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045288"
---
# <a name="metafile-extension-guidelines"></a>Linee guida sull'estensione metafile

Un'estensione di file fornisce un fornitore di software indipendente (ISV) con informazioni sui requisiti di rendering di un'applicazione che usa l'estensione e consente agli autori di contenuti di specificare come destinazione i tipi di giocatori generali.

Le estensioni del nome Metafile di Windows Media vengono usate per identificare il formato dei file di Windows Media a cui fa riferimento un metafile. I metafile di Windows Media con estensione Wax, wvx o ASX fanno riferimento rispettivamente ai file con estensione WMA, WMV e ASF. Tutti i metafile, indipendentemente dall'estensione del nome di file usato, hanno il tag dell'elemento **ASX** all'inizio del file con l'attributo **Version** specificato.

La tabella seguente illustra i tipi di file multimediali a cui fa riferimento ogni tipo di estensione del nome di file del metafile. Le colonne elencano le estensioni dei file multimediali, ovvero le estensioni dell'elenco di righe. Una X in una colonna indica un tipo di file multimediale a cui è possibile fare riferimento da una particolare estensione del nome di file Metafile.



| Estensione | .asf | wma | wmv |
|-----------|------|------|------|
| . wvx      | X    | X    | X    |
| . Wax      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Estensioni di file**](file-name-extensions.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




