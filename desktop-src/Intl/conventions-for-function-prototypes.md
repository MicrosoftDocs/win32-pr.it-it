---
description: L Windows SDK fornisce prototipi di funzione in versioni generiche, Windows tabella codici e Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Convenzioni per prototipi di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd37171ed4cd1f0f00267b935ec57f17ef2957514b63d770efdc851b9c08bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746141"
---
# <a name="conventions-for-function-prototypes"></a>Convenzioni per prototipi di funzione

L Windows SDK fornisce prototipi di funzione nelle versioni generiche, [Windows tabella codici](code-pages.md)e [Unicode.](unicode.md) I prototipi possono essere compilati per produrre Windows di tabella codici o prototipi Unicode. Tutti e tre i prototipi sono descritti in questo argomento e sono illustrati dagli esempi di codice per la [**funzione SetWindowText.**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)

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



Il preprocessore espande la macro nella tabella codici Windows o nel nome della funzione Unicode. La lettera "A" (ANSI) o "W" (Unicode) viene aggiunta alla fine del nome della funzione generica, in base alle esigenze. Il file di intestazione fornisce quindi due prototipi specifici, uno per Windows tabelle codici e uno per Unicode, come illustrato negli esempi seguenti.


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



Come illustrato in [Windows di dati](windows-data-types-for-strings.md)per le stringhe , il prototipo di funzione generica usa il tipo di dati LPCTSTR per il parametro di testo. Tuttavia, il prototipo della tabella codici di Windows utilizza il tipo LPCSTR e il prototipo Unicode utilizza LPCWSTR.

Per tutte le funzioni con argomenti di testo, le applicazioni devono in genere utilizzare i prototipi di funzione generici. Se un'applicazione definisce "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione, le istruzioni verranno compilate in funzioni Unicode.

> [!Note]  
> Le Windows devono usare Unicode per evitare le incoerenze di diverse pagine di codice e per semplificare la localizzazione. Devono essere scritti con funzioni generiche e devono definire UNICODE per compilare le funzioni in funzioni Unicode. Nelle poche posizioni in cui un'applicazione deve usare dati di tipo carattere a 8 bit, può usare in modo esplicito le funzioni per Windows di codice.

 

L'applicazione deve sempre utilizzare un prototipo di funzione generico con tipi di carattere e di stringa generici. Tutti i nomi di funzione che terminano con una "W" maiuscola accettano Unicode, ovvero parametri con caratteri wide. Alcune funzioni esistono solo nelle versioni Unicode e possono essere usate solo con i tipi di dati appropriati. Ad esempio, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) e [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) hanno solo versioni Unicode.

La sezione Requisiti della documentazione di riferimento per ogni funzione Unicode e set di caratteri fornisce informazioni sulle versioni delle funzioni implementate dai sistemi operativi supportati. Se viene inclusa una riga che inizia con "Unicode", la funzione ha versioni unicode e Windows tabella codici separate.

> [!Note]  
> Quando una funzione ha un parametro length per una stringa di caratteri, la lunghezza deve essere documentata come conteggio dei valori TCHAR nella stringa. Questo tipo di dati fa riferimento ai byte Windows delle versioni della tabella codici della funzione o alle parole a 16 bit per le versioni Unicode. Tuttavia, le funzioni che richiedono o restituiscono puntatori a blocchi di memoria non tipiti, ad esempio la funzione [**GlobalAlloc,**](/windows/win32/api/winbase/nf-winbase-globalalloc) in genere accettano una dimensione in byte, indipendentemente dal prototipo usato. Se l'allocazione di memoria non tipica è per una stringa, l'applicazione deve moltiplicare il numero di caratteri per sizeof(TCHAR). Per altre informazioni, vedere [Uso di tipi di dati generici.](using-generic-data-types.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
