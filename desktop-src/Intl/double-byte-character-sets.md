---
description: Un set di caratteri a due byte (DBCS), noto anche come set di caratteri &\# 0034 espanso a 8 bit&0034;, è un set di caratteri a byte singolo esteso (SBCS), implementato come tabella \# codici.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Set di caratteri a byte doppio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbef827b91c5ed2468b06f759883c0ba0b874e74038871227aabe0f65f1a046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147664"
---
# <a name="double-byte-character-sets"></a>Set di caratteri a byte doppio

Un set di caratteri a byte doppio (DBCS), noto anche come "set di caratteri espanso a 8 bit", è un [set](single-byte-character-sets.md) di caratteri a byte singolo esteso (SBCS), implementato come tabella codici. I DBCS sono stati originariamente sviluppati per estendere la progettazione SBCS per gestire lingue come il giapponese e il cinese. Alcuni caratteri in un DBCS, incluse le cifre e le lettere usate per la scrittura dell'inglese, hanno valori di codice a byte singolo. Altri caratteri, ad esempio ideogrammo cinese o kanji giapponese, hanno valori di codice a byte doppio. Un DBCS può corrispondere a una tabella Windows tabella codici o a una tabella codici OEM. Una tabella codici DBCS può includere anche una tabella codici non nativa, ad esempio una tabella codici EBCDIC. Per le definizioni di queste pagine codici, vedere [Code Pages.](code-pages.md)

> [!Note]  
> Le Windows devono usare [Unicode](unicode.md) per evitare le incoerenze di diverse pagine di codice e per semplificare la localizzazione. Tuttavia, alcuni protocolli legacy potrebbero richiedere l'uso di tabella codici DBCS. Ogni tabella codici DBCS supporta caratteri diversi, ma nessuna pagina supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici DBCS supporta un subset diverso, codificato in modo diverso. I dati convertiti da una tabella codici DBCS a un'altra sono soggetti a danneggiamento perché lo stesso valore di dati in diverse pagine di codice può codificare un carattere diverso. I dati convertiti da Unicode a DBCS sono soggetti a perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere usato in dati Unicode specifici.

 

Per interpretare una stringa DBCS, un'applicazione deve iniziare all'inizio della stringa ed eseguire l'analisi in avanti. Tiene traccia quando rileva un byte iniziale nella stringa e considera il byte successivo come parte finale dello stesso carattere. Se l'applicazione analizza semplicemente la stringa un byte alla volta e rileva un byte che sembra essere il valore di codice che rappresenta una barra rovesciata (" "), tale byte potrebbe essere semplicemente il byte finale di un carattere a \\ due byte. L'applicazione non può semplicemente eseguire il backup di un byte per verificare se il byte precedente è un byte di primo livello, perché tale valore di byte potrebbe essere idoneo per l'uso sia come byte iniziale che come byte finale. Di conseguenza, l'applicazione presenta essenzialmente lo stesso problema che con la possibile barra rovesciata. In altre parole, le ricerche di sottostringhe sono molto più complesse con un DBCS rispetto a SBCS o Unicode. Di conseguenza, le applicazioni che supportano un DBCS devono usare funzioni speciali, ad esempio [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), anziché [**la funzione StrStr.**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx)

Le applicazioni usano DBCS Windows di codice con le versioni "A" Windows funzioni. Vedere [Convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md) e le pagine [codici.](code-pages.md) Per identificare una tabella codici DBCS, un'applicazione può usare la [**funzione GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Un'applicazione può usare la [**funzione IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) per determinare se un determinato valore può essere usato come byte di inizio di un carattere a 2 byte. Inoltre, un'applicazione può usare le [**funzioni MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire il mapping tra stringhe Unicode e DBCS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> <dt>

[Set di caratteri a byte singolo](single-byte-character-sets.md)
</dt> </dl>

 

 
