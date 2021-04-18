---
description: 'Le funzioni API Windows che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode nell'API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314801"
---
# <a name="unicode-in-the-windows-api"></a>Unicode nell'API Windows

Le funzioni API Windows che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:

-   Versione generica che può essere compilata per le tabelle codici di Windows o Unicode
-   Una versione della [tabella codici di Windows](code-pages.md) con la lettera "a" usata per indicare "ANSI"
-   Una versione [Unicode](unicode.md) con la lettera "W" utilizzata per indicare "wide"

Alcune funzioni più recenti supportano solo versioni Unicode. Per altre informazioni, vedere [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).

Negli argomenti seguenti vengono illustrati i tipi di dati Unicode e il modo in cui vengono utilizzati in funzioni e messaggi. l'uso di risorse, nomi file e argomenti della riga di comando; metodi e per la conversione tra tipi diversi di stringhe.

-   [Traduzione automatica di messaggi](automatic-message-translation.md)
-   [Set di caratteri utilizzati nei nomi file](character-sets-used-in-file-names.md)
-   [Argomenti della riga di comando](command-line-arguments.md)
-   [Convenzioni per prototipi di funzione](conventions-for-function-prototypes.md)
-   [Funzioni C standard](standard-c-functions.md)
-   [Differenze tra le funzioni di stringa](string-function-differences.md)
-   [Conversione tra tipi di stringa](translation-between-string-types.md)
-   [Tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



