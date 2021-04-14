---
title: Annidamento di metafile
description: Annidamento di metafile
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Metafile di Windows Media, annidamento
- Metafile di Windows Media, che fanno riferimento ad altri metafile
- annidamento di metafile
- Metafile, annidamento
- Metafile, che fanno riferimento ad altri metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328575"
---
# <a name="nesting-metafiles"></a>Annidamento di metafile

Un metafile può fare riferimento A un altro metafile. Per fare riferimento a un altro metafile, usare l'elemento **ENTRYREF** . Un elemento **ENTRYREF** nel metafile primario punta a un metafile esterno.

Il controllo Windows Media Player elabora gli elementi **entry** del metafile a cui si fa riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF** . Tuttavia, ignora qualsiasi elemento **entry** nel metafile a cui si fa riferimento con l'attributo **SKIPIFREF** impostato su Yes.

I controlli Windows Media Player 7,0, 7,1 e Windows Media Player per Windows XP ignorano tutti gli elementi **ENTRYREF** nel metafile a cui si fa riferimento. Di conseguenza, i metafile possono essere annidati un solo livello di profondità usando queste versioni. Queste versioni ignorano anche l'elemento **ASX** e i relativi attributi nel file a cui si fa riferimento. Windows Media Player 9 Series o versioni successive supporta la nidificazione di metafile fino a 5 Deep.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> </dl>

 

 




