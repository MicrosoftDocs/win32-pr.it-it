---
description: 'Windows Le funzioni API che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode nell'API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c36e1e292eddd786d4c4bf336f980486f66870deb809587f9c51334f269ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764811"
---
# <a name="unicode-in-the-windows-api"></a>Unicode nell'API Windows

Windows Le funzioni API che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:

-   Una versione generica che può essere compilata per Windows tabella codici o Unicode
-   Versione [Windows tabella codici](code-pages.md) con la lettera "A" usata per indicare "ANSI"
-   Versione [Unicode](unicode.md) con la lettera "W" usata per indicare "wide"

Alcune funzioni più recenti supportano solo le versioni Unicode. Per altre informazioni, vedere [Convenzioni per i prototipi di funzione.](conventions-for-function-prototypes.md)

Negli argomenti seguenti vengono illustrati i tipi di dati Unicode e il modo in cui vengono utilizzati nelle funzioni e nei messaggi. l'uso di risorse, nomi di file e argomenti della riga di comando; e metodi per la conversione tra tipi diversi di stringhe.

-   [Conversione automatica dei messaggi](automatic-message-translation.md)
-   [Set di caratteri usati nei nomi di file](character-sets-used-in-file-names.md)
-   [Argomenti della riga di comando](command-line-arguments.md)
-   [Convenzioni per prototipi di funzione](conventions-for-function-prototypes.md)
-   [Funzioni C standard](standard-c-functions.md)
-   [Differenze tra le funzioni stringa](string-function-differences.md)
-   [Conversione tra tipi stringa](translation-between-string-types.md)
-   [Tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



