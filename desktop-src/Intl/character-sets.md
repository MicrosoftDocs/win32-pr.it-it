---
description: Un &\# 0034;set di caratteri&0034; è un mapping di caratteri ai relativi valori \# di codice di identificazione.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Character Sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f9bb57dad6924e2bbc9390d7315dbed0c59647cacefb932d7055ea8fdd3385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898801"
---
# <a name="character-sets"></a>Character Sets

Un "set di caratteri" è un mapping di caratteri ai relativi valori di codice di identificazione. Il set di caratteri attualmente usato più comunemente nei computer [è Unicode,](unicode.md)uno standard globale per la codifica dei caratteri. Internamente, le Windows usano l'implementazione UTF-16 di Unicode. In UTF-16 la maggior parte dei caratteri è identificata da codici a due byte. I caratteri supplementari meno comunemente usati sono rappresentati da una coppia di surrogati, ovvero una coppia di codici a due byte. Per altre informazioni, vedere [Surrogati e caratteri supplementari.](surrogates-and-supplementary-characters.md)

Alcune Windows applicazioni devono funzionare con i set di caratteri meno recenti nativi Windows Me/98/95. [Windows code pages consentono](code-pages.md) all'applicazione di usare questi set di caratteri. Questi set di caratteri possono essere suddivisi in:

-   [Set di caratteri a byte singolo](single-byte-character-sets.md) (SBCS). In un SBCS ogni carattere è identificato da un valore di un byte.
-   Set di caratteri multibyte, in particolare [i set di caratteri a byte doppio](double-byte-character-sets.md) (DBCS). I set di caratteri multibyte consentono di rappresentare il numero elevato di caratteri in molte lingue dell'Asia.

Per altre informazioni, vedere i seguenti argomenti:

-   [Code Pages](code-pages.md)
-   [Set di caratteri a byte doppio](double-byte-character-sets.md)
-   [Set di caratteri a byte singolo](single-byte-character-sets.md)
-   [Surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



