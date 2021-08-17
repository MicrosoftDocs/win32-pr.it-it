---
description: La maggior parte delle operazioni sulle stringhe può usare la stessa logica per Unicode e per Windows code pages.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipi di dati di Windows per le stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bef3dc98b7b8649b6cb0fc5bd9450c6f22c8b2bb6e3345790dab0dd24587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146814"
---
# <a name="windows-data-types-for-strings"></a>Tipi di dati di Windows per le stringhe

La maggior parte delle operazioni sulle stringhe può usare la stessa logica per [Unicode](unicode.md) e per Windows [code pages](code-pages.md). L'unica differenza è che l'unità operativa di base è un carattere a 16 bit (noto anche come carattere wide) per Unicode e un carattere a 8 bit per le Windows codici. I Windows di intestazione forniscono diverse definizioni di tipo che semplificano la creazione di origini che possono essere compilate per Unicode o per Windows code pages.

Windows supporta tre set di tipi di dati carattere e stringa: un set di definizioni di tipo generico che possono essere compilate per le code pages Unicode o Windows e due set di definizioni di tipo specifiche. Un set di definizioni di tipo specifiche è da usare con Unicode e l'altro è per l'uso con Windows code pages.

Un'applicazione che usa tipi di dati generici può essere compilata per Unicode semplicemente definendo "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione. Le Windows devono usare Unicode per evitare le incoerenze di diverse code pages e semplificare la localizzazione. Devono essere scritti con tipi di dati generici e devono definire "UNICODE" per compilare questi tipi in tipi Unicode. Nelle poche posizioni in cui un'applicazione deve usare dati di tipo carattere a 8 bit, può usare esplicitamente i tipi per le Windows code pages.

La possibilità di compilare i tipi generici in tipi per Windows code pages esiste principalmente per supportare le applicazioni legacy. Per compilare Windows code pages, l'applicazione omette semplicemente la definizione UNICODE.

Nell'esempio seguente viene illustrato il metodo usato nei Windows di intestazione per definire i tre set di tipi di dati. Per l'implementazione, vedere il file di intestazione Winnt.h.


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



La lettera "T" in una definizione di tipo, ad esempio TCHAR o LPTSTR, definisce un tipo generico che può essere compilato per Windows code pages o Unicode. La lettera "W" in una definizione di tipo, ad esempio WCHAR o LPWSTR, definisce un tipo Unicode. Poiché Windows code pages hanno il formato precedente, hanno definizioni di tipo semplice, ad esempio CHAR e LPSTR. Per una descrizione completa dei tipi di dati in Windows, vedere Windows [tipi di dati](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
