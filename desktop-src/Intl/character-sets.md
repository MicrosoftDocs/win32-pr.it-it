---
description: Un &\# 0034; set di caratteri&\# 0034; è un mapping di caratteri ai rispettivi valori di codice di identificazione.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Character Sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306611"
---
# <a name="character-sets"></a>Character Sets

Un "set di caratteri" è un mapping di caratteri ai rispettivi valori di codice di identificazione. Il set di caratteri usato più di frequente nei computer attualmente è [Unicode](unicode.md), uno standard globale per la codifica dei caratteri. Internamente, le applicazioni Windows utilizzano l'implementazione UTF-16 di Unicode. In UTF-16 la maggior parte dei caratteri è identificata da codici a due byte. I caratteri supplementari utilizzati meno di frequente sono rappresentati da una coppia di surrogati, ovvero una coppia di codici a due byte. Per ulteriori informazioni, vedere [surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md).

Alcune applicazioni Windows devono funzionare con i set di caratteri meno recenti nativi di Windows Me/98/95. Le [tabelle codici di Windows](code-pages.md) consentono all'applicazione di usare questi set di caratteri. Questi set di caratteri possono essere divisi in:

-   [Set di caratteri a byte singolo](single-byte-character-sets.md) (SBCS). In un SBCS ogni carattere viene identificato da un valore a una larghezza di byte.
-   Set di caratteri multibyte, in particolare i [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS). I set di caratteri multibyte forniscono un mezzo per rappresentare il numero elevato di caratteri in molte lingue asiatiche.

Per altre informazioni, vedere i seguenti argomenti:

-   [Tabelle codici](code-pages.md)
-   [Set di caratteri a byte doppio](double-byte-character-sets.md)
-   [Set di caratteri a byte singolo](single-byte-character-sets.md)
-   [Surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



