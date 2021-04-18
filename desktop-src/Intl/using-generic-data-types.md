---
description: Se si utilizzano tipi di dati generici nel codice, è possibile compilarli per Unicode semplicemente utilizzando una direttiva per il preprocessore per definire &\# 0034; UNICODE&\# 0034; prima delle \# istruzioni include per i file di intestazione.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Utilizzo di tipi di dati generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319481"
---
# <a name="using-generic-data-types"></a>Utilizzo di tipi di dati generici

Se si utilizzano tipi di dati generici nel codice, è possibile compilarli per [Unicode](unicode.md) semplicemente utilizzando una direttiva per il preprocessore per definire "Unicode" prima delle istruzioni **\# include** per i file di intestazione. Per compilare le [tabelle codici ANSI (code for Windows)](code-pages.md), omettere la definizione "Unicode". Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e semplificare la localizzazione.

Per creare codice sorgente che può essere compilato per l'utilizzo di caratteri e stringhe Unicode o per l'utilizzo di caratteri e stringhe dalle tabelle codici di Windows:

1.  Utilizzare tipi di dati generici, ad esempio TCHAR, LPTSTR e LPTCH, per tutti i tipi di carattere e stringa utilizzati per il testo. Per ulteriori informazioni sui tipi generici, vedere [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md).
2.  Assicurarsi che i puntatori a buffer di dati non di testo o matrici di byte binari siano codificati con tipi di dati, ad esempio LPBYTE o LPWORD, anziché il tipo LPTSTR o LPTCH.
3.  Dichiarare i puntatori del tipo indeterminato in modo esplicito come puntatori void usando LPVOID nel modo appropriato.
4.  Rendere indipendente dal tipo aritmetico del puntatore. L'uso di unità di dimensioni TCHAR restituisce variabili che sono 2 byte se è definito UNICODE e 1 byte se UNICODE non è definito. L'uso dell'aritmetica dei puntatori restituisce sempre il numero di elementi indicati dal puntatore, se le dimensioni degli elementi sono pari a 1 o 2 byte. L'espressione seguente recupera sempre il numero di elementi, indipendentemente dal fatto che sia definito UNICODE.

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    L'espressione seguente determina il numero di byte utilizzati.

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    Non è necessario modificare un'istruzione come quella riportata di seguito, perché l'incremento del puntatore punta all'elemento del carattere successivo.

    ```C++
    chNext = *++lpText;
    ```

    

5.  Sostituire stringhe letterali e costanti carattere manifesto con macro. Modificare le espressioni come quelle riportate di seguito.

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    Usare la macro di [**testo**](/windows/desktop/api/Winnt/nf-winnt-text) come indicato di seguito in questa espressione.

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    La macro di [**testo**](/windows/desktop/api/Winnt/nf-winnt-text) causa la valutazione delle stringhe come L "stringa" quando viene definito Unicode e come "stringa" in caso contrario. Per una gestione più semplice, spostare le stringhe letterali in risorse, soprattutto se contengono caratteri non compresi nell'intervallo ASCII (da 0x00 a 0x7F) o vengono esposti nell'interfaccia utente. Per supportare la localizzazione dell'applicazione per diverse lingue nazionali, è molto importante che tutte le stringhe dell'interfaccia utente siano in risorse localizzabili.

6.  Usare le versioni generiche delle funzioni di Windows. Per altre informazioni, vedere [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).
7.  Usare le versioni generiche delle funzioni stringa della libreria C standard e ricordare di definire " \_ Unicode" e "Unicode", come descritto in [funzioni C standard](standard-c-functions.md).
8.  Se si sta adattando un'applicazione originariamente scritta per le tabelle codici di Windows, ricordarsi di modificare il codice che si basa su 255 come valore più grande per un carattere.

Quando si compila il codice scritto come descritto in precedenza, il compilatore può creare sia la versione Unicode che la tabella codici di Windows dell'applicazione dalla stessa origine. A seconda delle definizioni per UNICODE, le funzioni generiche vengono risolte per produrre gli stessi file binari come se fosse stato scritto codice esclusivamente per Unicode o solo per le tabelle codici di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



