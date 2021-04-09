---
description: Un set di caratteri a byte singolo (SBCS) è un mapping di 256 singoli caratteri ai rispettivi valori di codice di identificazione, implementati come tabella codici.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Set di caratteri a byte singolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968593"
---
# <a name="single-byte-character-sets"></a>Set di caratteri a byte singolo

Un set di caratteri a byte singolo (SBCS) è un mapping di 256 singoli caratteri ai rispettivi valori di codice di identificazione, implementati come tabella codici. Un SBCS può corrispondere a una tabella codici di Windows o a una tabella codici OEM. Una tabella codici SBCS può includere anche una tabella codici non nativa, ad esempio una tabella codici EBCDIC. Per le definizioni di queste tabelle codici, vedere [tabelle codici](code-pages.md).

> [!Note]  
> Le nuove applicazioni Windows devono utilizzare [Unicode](unicode.md) per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione. Tuttavia, alcuni protocolli legacy richiedono l'uso di un SBCS. Ogni tabella codici SBCS supporta caratteri diversi, ma nessuna pagina supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici SBCS supporta un subset diverso, codificato in modo diverso. I dati convertiti da una tabella codici SBCS a un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in tabelle codici diverse può codificare un carattere diverso. I dati convertiti da Unicode a SBCS sono soggetti alla perdita di dati perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato in tali dati Unicode particolari.

 

Le applicazioni usano le tabelle codici di Windows SBCS con le versioni "A" delle funzioni di Windows. Vedere [convenzioni per prototipi di funzione](conventions-for-function-prototypes.md) e [tabelle codici](code-pages.md). Per semplificare l'identificazione di una tabella codici SBCS, un'applicazione può utilizzare la funzione [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Inoltre, un'applicazione può utilizzare le funzioni [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire il mapping tra le stringhe Unicode e SBCS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> <dt>

[Set di caratteri a byte doppio](double-byte-character-sets.md)
</dt> </dl>

 

 



