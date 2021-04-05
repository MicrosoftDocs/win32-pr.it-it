---
title: Supporto ID3
description: ID3 è un'organizzazione che ha definito un set di standard per l'inclusione dei metadati nei file audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK, supporto ID3
- ASF (Advanced Systems Format), supporto ID3
- ASF (Advanced Systems Format), supporto ID3
- metadati, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f356dae63b1d3672b584bb61956f478b67a697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713369"
---
# <a name="id3-support"></a>Supporto ID3

ID3 è un'organizzazione che ha definito un set di standard per l'inclusione dei metadati nei file audio MPEG Layer-3 (MP3). Gli oggetti di Windows Media Format SDK forniscono supporto per gli attributi compatibili con ID3. Sono supportate tre diverse versioni ID3: ID3v1. x, ID3v 2.2 e ID3v 2.3/v2, 4. Per un elenco degli attributi che corrispondono ai frame ID3, vedere Supporto di [tag ID3](id3-tag-support.md).

Se non specificato diversamente, non viene eseguita alcuna convalida dei dati del frame ID3 da parte degli oggetti di questo SDK. Ad esempio, l'attributo dei metadati [**WM/lyrics \_ sincronizzato**](wm-lyrics-synchronised.md) archivia i lyrics del brano con i timestamp corrispondenti. Quando si scrive un attributo di tipo **WM/lyrics \_ sincronizzato** , gli oggetti di questo SDK non verificheranno che i timestamp siano in ordine cronologico o eseguano la convalida di qualsiasi tipo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Funzionalità dei metadati**](metadata-features.md)
</dt> <dt>

[**Utilizzo dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




