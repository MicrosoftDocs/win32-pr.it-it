---
description: Se si usano tipi di dati generici nel codice, è possibile compilarlo per Unicode semplicemente usando una direttiva del preprocessore per definire &\# 0034; Unicode&\# 0034; prima delle \# istruzioni include per i file di intestazione.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Uso di tipi di dati generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a61bed094506f0d31718b0b88fe519028ba1db785ebda3e00404a7aa3257e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535462"
---
# <a name="using-generic-data-types"></a>Uso di tipi di dati generici

Se si usano tipi di dati generici nel codice, è possibile compilarlo per [Unicode](unicode.md) semplicemente usando una direttiva del preprocessore per definire "UNICODE" prima delle istruzioni **\# di** inclusione per i file di intestazione. Per compilare il codice [per Windows (ANSI),](code-pages.md)omettere la definizione "UNICODE". Le Windows devono usare Unicode per evitare le incoerenze di diverse code pages e semplificare la localizzazione.

Per creare codice sorgente che può essere compilato per usare caratteri e stringhe Unicode o per usare caratteri e stringhe da Windows code pages:

1.  Usare tipi di dati generici, ad esempio TCHAR, LPTSTR e LPTCH, per tutti i tipi di carattere e stringa usati per il testo. Per altre informazioni sui tipi generici, [Windows tipi di dati per le stringhe](windows-data-types-for-strings.md).
2.  Assicurarsi che i puntatori a buffer di dati non di testo o matrici di byte binari siano codificati con tipi di dati, ad esempio LPBYTE o LPWORD, anziché con il tipo LPTSTR o LPTCH.
3.  Dichiarare in modo esplicito i puntatori di tipo indeterminato come puntatori void usando LPVOID in base alle esigenze.
4.  Rendere indipendente dal tipo aritmetico del puntatore. L'uso di unità di dimensioni TCHAR produce variabili di 2 byte se è definito UNICODE e 1 byte se UNICODE non è definito. L'uso dell'aritmetica dei puntatori restituisce sempre il numero di elementi indicati dal puntatore, indipendentemente dal fatto che le dimensioni degli elementi siano di 1 o 2 byte. L'espressione seguente recupera sempre il numero di elementi, indipendentemente dal fatto che UNICODE sia definito.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    L'espressione seguente determina il numero di byte utilizzati.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Non è necessario modificare un'istruzione come la seguente, perché l'incremento del puntatore punta all'elemento carattere successivo.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Sostituire le stringhe letterali e le costanti di caratteri manifesto con macro. Modificare espressioni come la seguente.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Usare la macro [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) come indicato di seguito in questa espressione.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    La macro [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) determina la valutazione delle stringhe come L"string" quando viene definito UNICODE e come "string" in caso contrario. Per semplificare la gestione, spostare le stringhe letterali nelle risorse, in particolare se contengono caratteri non compreso nell'intervallo ASCII (da 0x00 a 0x7F) o sono esposte nell'interfaccia utente. Per supportare la localizzazione dell'applicazione per lingue nazionali diverse, è molto importante che tutte le stringhe dell'interfaccia utente siano in risorse localizzabili.

6.  Usare le versioni generiche delle funzioni Windows generiche. Per altre informazioni, vedere [Convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).
7.  Usare le versioni generiche delle funzioni stringa della libreria C standard e ricordare di definire "UNICODE" e "UNICODE", come descritto \_ in Funzioni C [standard](standard-c-functions.md).
8.  Se si adatta un'applicazione scritta originariamente per Windows code pages, ricordarsi di modificare qualsiasi codice che si basa su 255 come valore più grande per un carattere.

Quando si compila codice scritto come descritto in precedenza, il compilatore può creare sia versioni della tabella codici Unicode che Windows della tabella codici dell'applicazione dalla stessa origine. A seconda delle definizioni per UNICODE, le funzioni generiche vengono risolte per produrre gli stessi file binari come se fosse stato scritto codice esclusivamente per Unicode o esclusivamente per Windows code pages.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di unicode e set di caratteri](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



