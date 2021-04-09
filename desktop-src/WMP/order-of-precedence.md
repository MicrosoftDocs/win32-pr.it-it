---
title: Ordine di precedenza
description: Ordine di precedenza
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Metafile di Windows Media, ordine di precedenza
- Metafile di Windows Media, precedenza
- Metafile, ordine di precedenza
- Metafile, precedenza
- Windows Media, metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044367"
---
# <a name="order-of-precedence"></a>Ordine di precedenza

Non tutti gli attributi dell'elemento metafile vengono creati uguali. Alcuni attributi dell'elemento metafile eseguono l'override di altri attributi dell'elemento. Gli attributi degli elementi possono essere sottoposti a override da attributi di elementi simili a seconda della posizione e dell'ordine. Tutti gli attributi di una playlist di metafile eseguono l'override di quelli contenuti in un file Windows Media a cui si fa riferimento. Un attributo che esegue l'override di un altro ha precedenza maggiore.

La gerarchia, con la precedenza più alta a quella più bassa, è illustrata nella tabella seguente. L'elemento con precedenza più alta non viene mai sottoposto a override.



| Ambito                    | Gerarchia                                   |
|--------------------------|---------------------------------------------|
| "Contenuto DRM firmato"     | Mai sottoposto a override.                           |
| Ambito dell'elemento **ref**    | Sottoposto a override solo dal contenuto DRM firmato.      |
| Ambito elemento **voce**  | Esegue l'override degli elementi delle categorie seguenti. |
| Ambito **ASX**            | Esegue l'override degli elementi del file multimediale.              |
| Ambito file Windows Media | Sottoposto a override da tutti i precedenti.             |



 

-   "Contenuto DRM firmato": oggetto firma digitale.

    Gli attributi del contenuto DRM firmato eseguiranno l'override di tutti gli altri. Le informazioni sul copyright di "contenuto DRM firmato", ad esempio, non verranno sostituite. Verrà sempre trasmesso e visualizzato.

-   Ambito dell'elemento **ref**

    Gli attributi dell'elemento **ref** sostituiranno gli altri attributi degli elementi, ma non i contenuti DRM firmati.

-   Ambito **voce**

    Gli attributi dell'elemento **entry** verranno sottoposti a override dall'attributo dell'elemento **ref** , ma eseguiranno l'override di altri attributi dell'elemento. Vengono visualizzati i metadati del **titolo** dall'elemento **entry** anziché le informazioni sul titolo del file multimediale.

-   Ambito **ASX**

    Tutte le proprietà immesse nel metafile eseguono l'override di quelle contenute nel file di Windows Media. Attributi dell'elemento **entry** che eseguono l'override degli attributi degli elementi **ASX** . Mentre viene riprodotto il clip multimediale a cui viene fatto riferimento nell'elemento **entry** , vengono visualizzati i metadati del **titolo** dall'elemento **entry** anziché le informazioni sul titolo dell'elemento **ASX** .

-   Ambito file Windows Media

    Gli attributi del file Windows Media vengono sottoposti a override da qualsiasi attributo del metafile. I metadati del file multimediale vengono visualizzati solo se non sono stati definiti metadati per tale elemento nel metafile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




