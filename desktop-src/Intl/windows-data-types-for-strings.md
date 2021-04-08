---
description: La maggior parte delle operazioni di stringa può utilizzare la stessa logica per le tabelle codici Unicode e per Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Tipi di dati di Windows per le stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058358"
---
# <a name="windows-data-types-for-strings"></a>Tipi di dati di Windows per le stringhe

La maggior parte delle operazioni di stringa può utilizzare la stessa logica per le [tabelle codici](code-pages.md) [Unicode](unicode.md) e per Windows. L'unica differenza è che l'unità di base dell'operazione è un carattere a 16 bit (noto anche come carattere wide) per Unicode e un carattere a 8 bit per le tabelle codici di Windows. I file di intestazione di Windows forniscono diverse definizioni di tipi che semplificano la creazione di origini che possono essere compilate per Unicode o per le tabelle codici di Windows.

Windows supporta tre set di tipi di dati di tipo carattere e stringa: un set di definizioni di tipo generico che possono essere compilate per le tabelle codici Unicode o Windows e due set di definizioni di tipi specifiche. Un set di definizioni di tipi specifiche è da usare con Unicode e l'altro per l'uso con le tabelle codici di Windows.

Un'applicazione che usa tipi di dati generici può essere compilata per Unicode semplicemente definendo "UNICODE" prima delle istruzioni **\# include** per i file di intestazione o durante la compilazione. Le nuove applicazioni Windows devono utilizzare Unicode per evitare le incoerenze di diverse tabelle codici e semplificare la localizzazione. Devono essere scritti con tipi di dati generici e devono definire "UNICODE" per compilare questi tipi in tipi Unicode. Nelle poche posizioni in cui un'applicazione deve funzionare con dati di tipo carattere a 8 bit, può utilizzare esplicitamente i tipi per le tabelle codici di Windows.

La possibilità di compilare i tipi generici nei tipi per le tabelle codici di Windows esiste principalmente per supportare le applicazioni legacy. Per eseguire la compilazione per le tabelle codici di Windows, l'applicazione omette semplicemente la definizione UNICODE.

Nell'esempio seguente viene illustrato il metodo utilizzato nei file di intestazione di Windows per definire i tre set di tipi di dati. Per l'implementazione, vedere il file di intestazione Winnt. h.


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



La lettera "T" in una definizione di tipo, ad esempio TCHAR o LPTSTR, designa un tipo generico che può essere compilato per le tabelle codici di Windows o Unicode. La lettera "W" in una definizione di tipo, ad esempio WCHAR o LPWSTR, definisce un tipo Unicode. Poiché le tabelle codici di Windows sono del formato precedente, hanno definizioni di tipo semplice, ad esempio CHAR e LPSTR. Per una descrizione completa dei tipi di dati in Windows, vedere [tipi di dati di Windows](../winprog/windows-data-types.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
