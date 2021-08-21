---
title: Annidamento di metafile
description: Annidamento di metafile
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows metafile multimediali, annidamento
- Windows metafile multimediali, riferimento ad altri metafile
- annidamento di metafile
- metafile, annidamento
- metafile, riferimento ad altri metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29a45bf545f839e111970b31d5faddd039959b7148a331fa5e347913b67327e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574274"
---
# <a name="nesting-metafiles"></a>Annidamento di metafile

Un metafile può fare riferimento a un altro metafile. Per fare riferimento a un altro metafile, usare **l'elemento ENTRYREF.** Un **elemento ENTRYREF** nel metafile primario punta a un metafile esterno.

Il Windows Media Player elabora gli elementi **ENTRY** del metafile di riferimento come se fossero inclusi nel metafile primario nella posizione dell'elemento **ENTRYREF.** Tuttavia, ignora tutti gli elementi **ENTRY** nel metafile di riferimento con l'attributo **SKIPIFREF** impostato su YES.

I Windows Media Player 7.0, 7.1 e Windows Media Player per Windows XP ignorano tutti gli **elementi ENTRYREF** nel metafile a cui si fa riferimento. Di conseguenza, i metafile possono essere annidati a un solo livello usando queste versioni. Queste versioni ignorano anche **l'elemento ASX** e i relativi attributi nel file di riferimento. Windows Media Player serie 9 o successive supporta l'annidamento di metafile fino a 5.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist metafile**](creating-metafile-playlists.md)
</dt> </dl>

 

 




