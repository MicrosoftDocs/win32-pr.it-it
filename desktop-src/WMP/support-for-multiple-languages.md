---
title: Supporto per più lingue
description: Supporto per più lingue
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Playlist Windows Media Metafile, supporto per più lingue
- playlist di metafile, supporto per più lingue
- playlist, supporto per più lingue
- Playlist Windows Media Metafile, supporto per più lingue
- playlist di metafile, supporto per più linguaggi
- playlist, supporto per più lingue
- Playlist Windows Media Metafile, supporto linguistico
- playlist di metafile, supporto del linguaggio
- playlist, supporto linguistico
- supporto per più lingue
- supporto multilingue
- supporto delle lingue
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045195"
---
# <a name="support-for-multiple-languages"></a>Supporto per più lingue

Windows Media Player 9 Series o versioni successive supporta i file multimediali di Windows creati utilizzando il set di caratteri Unicode. In questo modo è possibile includere metadati multilingue nella playlist del metafile. Le regole seguenti regolano l'utilizzo di metadati multilingue nei metafile multimediali di Windows:

-   I caratteri devono essere codificati con lo schema di codifica UTF-8.
-   La playlist del metafile deve includere il **param** seguente al livello della playlist:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Questa funzionalità è supportata solo in Windows Media Player 9 serie o versioni successive.
-   Se la playlist del metafile non viene salvata con la codifica UTF-8 e l'elemento **param** corretto, verrà analizzato utilizzando la tabella codici delle impostazioni locali di sistema predefinita del computer dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**PARAM (elemento)**](param-element.md)
</dt> <dt>

[**Cenni preliminari sui file di Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




