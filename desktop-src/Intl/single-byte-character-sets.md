---
description: Un set di caratteri a byte singolo (SBCS) è un mapping di 256 caratteri singoli ai relativi valori di codice di identificazione, implementato come tabella codici.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Set di caratteri a byte singolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bb0150dfaf2e3b8e8251530fd5e90e7b1ede3b3597d344e5efb192fa96ed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130231"
---
# <a name="single-byte-character-sets"></a>Set di caratteri a byte singolo

Un set di caratteri a byte singolo (SBCS) è un mapping di 256 caratteri singoli ai relativi valori di codice di identificazione, implementato come tabella codici. Una tabella codici SBCS può corrispondere a una Windows tabella codici o a una tabella codici OEM. Una tabella codici SBCS può includere anche una tabella codici non nativa, ad esempio una tabella codici EBCDIC. Per le definizioni di queste pagine codici, vedere [Code Pages.](code-pages.md)

> [!Note]  
> Le Windows devono usare [Unicode](unicode.md) per evitare le incoerenze di diverse pagine di codice e per semplificare la localizzazione. Tuttavia, alcuni protocolli legacy richiedono l'uso di un SBCS. Ogni tabella codici SBCS supporta caratteri diversi, ma nessuna pagina supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici SBCS supporta un subset diverso, codificato in modo diverso. I dati convertiti da una tabella codici SBCS a un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in diverse pagine di codice può codificare un carattere diverso. I dati convertiti da Unicode a SBCS sono soggetti a perdita di dati perché una determinata tabella codici potrebbe non essere in grado di rappresentare tutti i caratteri utilizzati nei dati Unicode specifici.

 

Le applicazioni usano SBCS Windows di codice con le versioni "A" Windows funzioni. Vedere [Convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md) e le pagine [codici.](code-pages.md) Per identificare una tabella codici SBCS, un'applicazione può usare la [**funzione GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Inoltre, un'applicazione può usare le [**funzioni MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire il mapping tra stringhe Unicode e SBCS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> <dt>

[Set di caratteri a byte doppio](double-byte-character-sets.md)
</dt> </dl>

 

 



