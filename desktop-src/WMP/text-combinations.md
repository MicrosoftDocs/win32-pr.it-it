---
title: Combinazioni di testo
description: Combinazioni di testo
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skin, combinazioni di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515841"
---
# <a name="text-combinations"></a>Combinazioni di testo

Questo valore è un elenco di combinazioni di caselle di testo, separate da virgole. Le caselle di visualizzazione del testo possono essere unite in join da un carattere più per creare un nuovo valore di visualizzazione Marquee e qualsiasi tipo di testo definito nella sezione tipo testo può essere usato nel Marquee.

Quando si determinano gli elementi da visualizzare, Windows Media Player mobile valuta ogni elemento dell'elenco per verificare se sono disponibili tutte le parti. In caso contrario, l'elemento successivo viene valutato e così via fino a quando non vengono trovate tutte le parti disponibili. Se, ad esempio, si desidera visualizzare autore e titolo, ma non si è certi che entrambi siano disponibili, utilizzare il valore seguente:


```C++
Title+Author, Title, Author

```



Nell'esempio precedente, il titolo + autore verrà visualizzato se il titolo e l'autore sono stati definiti per l'elemento multimediale. Se non sono definiti entrambi, il titolo viene valutato e visualizzato se definito. Se il titolo non è definito, l'autore viene visualizzato se definito. Se non viene definito alcun elemento, non viene visualizzato nulla.

Quando si usa il segno più per la concatenazione, assicurarsi di non avere spazi su entrambi i lati del segno più.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Testo scorrevole**](marquee.md)
</dt> <dt>

[**Tipo di testo**](text-type.md)
</dt> </dl>

 

 




