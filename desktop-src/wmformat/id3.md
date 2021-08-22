---
title: Supporto ID3
description: ID3 è un'organizzazione che ha definito un set di standard per includere i metadati nei file audio MPEG Layer-3 (MP3).
ms.assetid: 8c1f1114-48d8-4dce-b7ab-0293265a875c
keywords:
- Windows Media Format SDK, supporto ID3
- Advanced Systems Format (ASF), supporto ID3
- ASF (Advanced Systems Format),supporto ID3
- metadati, ID3
- ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c92fb9282483b6fd01b1149220e5f30421c3c1285bd533d64afef91709314e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702982"
---
# <a name="id3-support"></a>Supporto ID3

ID3 è un'organizzazione che ha definito un set di standard per includere i metadati nei file audio MPEG Layer-3 (MP3). Gli oggetti di Windows Media Format SDK forniscono il supporto per gli attributi compatibili con ID3. Sono supportate tre versioni ID3 distinte: ID3v1.x, ID3v2.2 e ID3v2.3/v2,4. Per un elenco degli attributi che equi equivaciano ai frame ID3, vedere [Supporto dei tag ID3.](id3-tag-support.md)

Se non specificato diversamente, non viene eseguita alcuna convalida dei dati dei frame ID3 dagli oggetti di questo SDK. Ad esempio, l'attributo di metadati [**WM/Lyrics \_ Synchronised**](wm-lyrics-synchronised.md) archivia il testo del brano con timestamp corrispondenti. Quando si scrive un attributo **\_ SYNCHronised di WM/Lyrics,** gli oggetti di questo SDK non verificano che i timestamp siano in ordine cronologico o esercitino la convalida di qualsiasi tipo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attributi**](attributes.md)
</dt> <dt>

[**Funzionalità dei metadati**](metadata-features.md)
</dt> <dt>

[**Uso dei metadati**](working-with-metadata.md)
</dt> </dl>

 

 




