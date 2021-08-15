---
title: Supporto per più lingue
description: Supporto per più lingue
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows playlist di metafile multimediali, supporto per più lingue
- playlist di metafile, supporto per più lingue
- playlist, supporto per più lingue
- Windows Playlist di metafile multimediali, supporto per più lingue
- playlist di metafile, supporto per più lingue
- playlist, supporto per più lingue
- Windows playlist di metafile multimediali, supporto della lingua
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002071"
---
# <a name="support-for-multiple-languages"></a>Supporto per più lingue

Windows Media Player 9 Series o versioni successive supporta Windows metafile multimediali creati usando il set di caratteri Unicode. In questo modo è possibile includere metadati multilingue nella playlist del metafile. Le regole seguenti regolano l'uso di metadati multilingue Windows metafile multimediali:

-   I caratteri devono essere codificati usando lo schema di codifica UTF-8.
-   La playlist del metafile deve includere il **parametro PARAM** seguente a livello di playlist:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Solo Windows Media Player serie 9 o successive supporta questa funzionalità.
-   Se la playlist del metafile non viene salvata con la codifica UTF-8 e l'elemento **PARAM** corretto, verrà analizzata usando la tabella codici delle impostazioni locali del sistema predefinite del computer dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Windows Panoramica dei metafile multimediali**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




