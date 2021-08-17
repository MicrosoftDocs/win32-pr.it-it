---
title: Ordine di precedenza
description: Ordine di precedenza
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Metafile multimediali, ordine di precedenza
- Windows Metafile multimediali, precedenza
- metafile, ordine di precedenza
- metafile, precedenza
- Windows Supporti, metafile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12b55f34dd18fa6122d3f1588111aaffe374f2d87c06ef9100cbac057efd4bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467992"
---
# <a name="order-of-precedence"></a>Ordine di precedenza

Non tutti gli attributi dell'elemento metafile vengono creati in modo uguale. Alcuni attributi degli elementi metafile eseguono l'override di altri attributi dell'elemento. Gli attributi degli elementi possono essere sottoposti a override da attributi di elemento simili a seconda della posizione e dell'ordine. Tutti gli attributi di una playlist di metafile eseguono l'override di quelli contenuti in un file Windows file multimediale di riferimento. Un attributo che esegue l'override di un altro ha precedenza più alta.

La gerarchia, con la precedenza più alta alla più bassa, è illustrata nella tabella seguente. L'elemento con precedenza più alta non viene mai sottoposto a override.



| Ambito                    | Gerarchia                                   |
|--------------------------|---------------------------------------------|
| "Contenuto DRM firmato"     | Mai sottoposto a override.                           |
| **Ambito dell'elemento REF**    | Sottoposto a override solo dal contenuto DRM firmato.      |
| **Ambito dell'elemento ENTRY**  | Esegue l'override degli elementi delle categorie seguenti. |
| **Ambito ASX**            | Esegue l'override degli elementi del file multimediale.              |
| Windows Ambito del file multimediale | Sottoposto a override da tutti gli elementi precedenti.             |



 

-   "Signed DRM content" (Contenuto DRM firmato) - Oggetto firma digitale.

    Gli attributi del contenuto DRM firmato eseguiranno l'override di tutti gli altri. Ad esempio, le informazioni sul copyright del "contenuto DRM firmato" non verranno sostituite. Verrà sempre trasmesso e presentato.

-   **Ambito dell'elemento REF**

    Gli attributi **dell'elemento REF** eseguiranno l'override di altri attributi dell'elemento, ma non del contenuto DRM firmato.

-   **Ambito ENTRY**

    Gli attributi **dell'elemento ENTRY** verranno sottoposti a override dall'attributo **dell'elemento REF,** ma eseguiranno l'override di altri attributi dell'elemento. **Vengono** visualizzati i **metadati TITLE** dell'elemento ENTRY anziché le informazioni sul titolo del file multimediale.

-   **Ambito ASX**

    Tutte le proprietà immesse nel metafile sostituiscono quelle contenute nel file Windows file multimediale. Gli attributi **dell'elemento ENTRY** eseguono l'override degli attributi **dell'elemento ASX.** Durante la riproduzione del clip multimediale di riferimento dell'elemento **ENTRY,** vengono visualizzati i metadati **TITLE** dell'elemento **ENTRY** anziché le informazioni sul titolo dell'elemento **ASX.**

-   Windows Ambito del file multimediale

    Gli attributi del Windows file multimediale vengono sostituiti da qualsiasi attributo metafile. I metadati del file multimediale vengono visualizzati solo se non sono presenti metadati definiti per tale elemento nel metafile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di playlist di metafile**](creating-metafile-playlists.md)
</dt> <dt>

[**Playlist di metafile**](metafile-playlists.md)
</dt> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




