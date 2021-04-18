---
description: Un set di caratteri DBCS (Double-byte character set), noto anche come &0034, un \# set di caratteri a 8 bit espanso&\# 0034;, è un set di caratteri a byte esteso (SBCS), implementato come tabella codici.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Set di caratteri a byte doppio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431b762b19f5531644e4bbaace548f34245c9d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317166"
---
# <a name="double-byte-character-sets"></a>Set di caratteri a byte doppio

Un set di caratteri DBCS (Double-byte character set), noto anche come "set di caratteri a 8 bit espanso", è un [set di caratteri a byte singolo](single-byte-character-sets.md) esteso (SBCS), implementato come tabella codici. I DBCS sono stati originariamente sviluppati per estendere la progettazione SBCS per la gestione di linguaggi come il giapponese e il cinese. Alcuni caratteri in un DBCS, inclusi i numeri e le lettere usati per la scrittura dell'inglese, hanno valori di codice a byte singolo. Altri caratteri, ad esempio ideogrammi cinesi o Kanji giapponese, hanno valori di codice a byte doppio. Un DBCS può corrispondere a una tabella codici di Windows o a una tabella codici OEM. Una tabella codici DBCS può includere anche una tabella codici non nativa, ad esempio una tabella codici EBCDIC. Per le definizioni di queste tabelle codici, vedere [tabelle codici](code-pages.md).

> [!Note]  
> Le nuove applicazioni Windows devono utilizzare [Unicode](unicode.md) per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione. Tuttavia, alcuni protocolli legacy possono richiedere l'utilizzo di tabelle codici DBCS. Ogni tabella codici DBCS supporta caratteri diversi, ma nessuna pagina supporta l'intera gamma di caratteri forniti da Unicode. Ogni tabella codici DBCS supporta un subset diverso, codificato in modo diverso. I dati convertiti da una tabella codici DBCS a un'altra sono soggetti a danneggiamento poiché lo stesso valore di dati in tabelle codici diverse può codificare un carattere diverso. I dati convertiti da Unicode a DBCS sono soggetti alla perdita di dati, perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato in tali dati Unicode particolari.

 

Per interpretare una stringa DBCS, un'applicazione deve iniziare all'inizio della stringa e quindi eseguire l'analisi in futuro. Tiene traccia del momento in cui incontra un byte iniziale nella stringa e considera il byte successivo come parte finale dello stesso carattere. Se l'applicazione analizza semplicemente la stringa un byte alla volta e rileva un byte che sembra essere il valore del codice che rappresenta una barra rovesciata (" \\ "), tale byte potrebbe essere semplicemente il byte finale di un carattere a due byte. L'applicazione non può solo eseguire il backup di un byte per verificare se il byte precedente è un byte iniziale, in quanto tale valore di byte potrebbe essere idoneo per essere utilizzato sia come byte iniziale che come byte finale. In questo modo, l'applicazione ha essenzialmente lo stesso problema con la barra rovesciata possibile. In altre parole, le ricerche di sottostringhe sono molto più complesse con un DBCS rispetto a SBCSs o Unicode. Di conseguenza, le applicazioni che supportano un DBCS devono usare funzioni speciali, ad esempio [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), invece della funzione [**StrStr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) .

Le applicazioni utilizzano le tabelle codici DBCS di Windows con le versioni "A" delle funzioni di Windows. Vedere [convenzioni per prototipi di funzione](conventions-for-function-prototypes.md) e [tabelle codici](code-pages.md). Per semplificare l'identificazione di una tabella codici DBCS, un'applicazione può utilizzare la funzione [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Un'applicazione può utilizzare la funzione [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) per determinare se un valore specificato può essere utilizzato come byte di apertura di un carattere a 2 byte. Inoltre, un'applicazione può utilizzare le funzioni [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire il mapping tra stringhe Unicode e DBCS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Character Sets](character-sets.md)
</dt> <dt>

[Set di caratteri a byte singolo](single-byte-character-sets.md)
</dt> </dl>

 

 
