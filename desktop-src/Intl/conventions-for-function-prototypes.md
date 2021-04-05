---
description: Il Windows SDK fornisce i prototipi di funzione in Generic, tabella codici di Windows e versioni Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenzioni per prototipi di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882149"
---
# <a name="conventions-for-function-prototypes"></a>Convenzioni per prototipi di funzione

Il Windows SDK fornisce i prototipi di funzione in Generic, [tabella codici di Windows](code-pages.md)e versioni [Unicode](unicode.md) . I prototipi possono essere compilati per produrre prototipi di tabella codici di Windows o prototipi Unicode. Tutti e tre i prototipi vengono descritti in questo argomento e sono illustrati dagli esempi di codice per la funzione [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .

Di seguito è riportato un esempio di prototipo generico:


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



Il file di intestazione fornisce il nome della funzione generica implementato come macro.


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



Il preprocessore espande la macro nella tabella codici di Windows o nel nome della funzione Unicode. La lettera "A" (ANSI) o "W" (Unicode) viene aggiunta alla fine del nome della funzione generica, a seconda dei casi. Il file di intestazione fornisce quindi due prototipi specifici, uno per le tabelle codici di Windows e uno per Unicode, come illustrato negli esempi seguenti.


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



Come illustrato in [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md), il prototipo di funzione generica usa il tipo di dati LPCTSTR per il parametro di testo. Tuttavia, il prototipo della tabella codici di Windows utilizza il tipo LPCSTR e il prototipo Unicode utilizza LPCWSTR.

Per tutte le funzioni con argomenti di testo, le applicazioni devono in genere utilizzare i prototipi di funzione generici. Se un'applicazione definisce "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione, le istruzioni verranno compilate in funzioni Unicode.

> [!Note]  
> Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione. Devono essere scritti con funzioni generiche ed è necessario definire UNICODE per compilare le funzioni in funzioni Unicode. Nelle poche posizioni in cui un'applicazione deve funzionare con dati di tipo carattere a 8 bit, può utilizzare esplicitamente le funzioni per le tabelle codici di Windows.

 

L'applicazione deve sempre utilizzare un prototipo di funzione generico con tipi di carattere e di stringa generici. Tutti i nomi di funzione che terminano con una "W" maiuscola accettano Unicode, ovvero parametri con caratteri wide. Alcune funzioni sono disponibili solo nelle versioni Unicode e possono essere utilizzate solo con i tipi di dati appropriati. Ad esempio, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) hanno solo versioni Unicode.

La sezione requisiti nella documentazione di riferimento per ogni funzione di set di caratteri e Unicode fornisce informazioni sulle versioni di funzione implementate dai sistemi operativi supportati. Se è inclusa una riga che inizia con "Unicode", la funzione dispone di versioni separate della tabella codici Unicode e di Windows.

> [!Note]  
> Quando una funzione ha un parametro di lunghezza per una stringa di caratteri, la lunghezza deve essere documentata come conteggio dei valori di TCHAR nella stringa. Questo tipo di dati fa riferimento a byte per le versioni della tabella codici di Windows della funzione o parole a 16 bit per le versioni Unicode. Tuttavia, le funzioni che richiedono o restituiscono puntatori a blocchi di memoria non tipizzata, ad esempio la funzione [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , in genere accettano una dimensione in byte, indipendentemente dal prototipo utilizzato. Se l'allocazione della memoria non tipizzata è per una stringa, l'applicazione deve moltiplicare il numero di caratteri per sizeof (TCHAR). Per ulteriori informazioni, vedere [utilizzo di tipi di dati generici](using-generic-data-types.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
