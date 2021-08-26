---
description: Le librerie di runtime C standard contengono entrambe le versioni UNICODE UTF-16 (caratteri wide) delle funzioni stringa che possono essere usate con le versioni Unicode e orientate ai byte delle funzioni stringa che possono essere usate con caratteri di set di caratteri a byte singolo (SBCS). Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar t in ANSI C e consente \_ l'accesso alle funzioni stringa Unicode. Le versioni Unicode delle funzioni iniziano con le lettere &\# 0034;wcs&\# 0034; (o talvolta &\# 0034; \_ wcs&\# 0034;). Il tipo di dati CHAR usato per le code pages è compatibile con il tipo di dati character char in ANSI C, per consentire l'accesso alle funzioni della stringa di caratteri. Le versioni dei caratteri delle funzioni iniziano con le lettere &\# 0034;str&\# 0034;. Esistono anche versioni speciali per i set di caratteri a byte doppio (DBCS) che iniziano con le lettere &\# 0034; \_ mbs&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funzioni C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e576dd8ad506d3d0f3379c161526dd7b9330542ca1cc575c95e3eda8e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130161"
---
# <a name="standard-c-functions"></a>Funzioni C standard

Le librerie di runtime C standard contengono entrambe le versioni UNICODE UTF-16 (caratteri wide) delle funzioni stringa che possono essere usate con [le](unicode.md) versioni Unicode e orientate ai byte delle funzioni stringa che possono essere usate con caratteri di set di caratteri a byte [singolo](single-byte-character-sets.md) (SBCS). Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar t in ANSI C e consente \_ l'accesso alle funzioni stringa Unicode. Le versioni Unicode delle funzioni iniziano con le lettere "wcs" (o talvolta " \_ wcs"). Il tipo di dati CHAR usato per le code pages è compatibile con il tipo di dati character char in ANSI C, per consentire l'accesso alle funzioni della stringa di caratteri. Le versioni dei caratteri delle funzioni iniziano con le lettere "str". Esistono anche versioni speciali per [i set di](double-byte-character-sets.md) caratteri a byte doppio (DBCS) che iniziano con le lettere " \_ mbs".

Le librerie di runtime C standard includono funzioni generiche per tutte le funzioni stringa C standard. Iniziano con \_ "tcs" e sono elencati nel file di intestazione Tchar.h. Queste funzioni usano il tipo di dati TCHAR generico.

Un'applicazione deve aggiungere le righe seguenti per usare le funzioni generiche e compilare per Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Si noti che sono necessari entrambi i file Tchar.h e Wchar.h e che è necessario anche il carattere di sottolineatura \_ iniziale nella variabile UNICODE. Questa nomenclatura è specifica della libreria C standard. Il rendering di "UNICODE" senza il carattere di sottolineatura è per i runtime Windows Microsoft.

Le [funzioni wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) e [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) possono eseguire la conversione dal set di caratteri supportato dalla libreria C standard a Unicode e versioni precedenti, con alcune limitazioni. Per altre informazioni sulla conversione di stringhe da e verso Unicode, vedere [Conversione tra tipi di stringa.](translation-between-string-types.md)

La [funzione printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definita in Tchar.h supporta le stesse specifiche di formato delle funzioni di stampa Strsafe.h, ad esempio [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). Analogamente, Tchar.h definisce una [funzione wprintf,](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) in cui la stringa di formato stessa è una stringa Unicode.

> [!Caution]  
> Una gestione insufficiente del buffer è implicata in molti problemi di sicurezza che comportano sovraccarichi del buffer. Vedere [Strsafe.h Reference (Informazioni di riferimento su Strsafe.h).](../menurc/strsafe-ovw.md) Le funzioni definite in Strsafe.h forniscono un'elaborazione aggiuntiva per la corretta gestione del buffer nel codice. Hanno lo scopo di sostituire le controparti C/C++ incorporate e specifiche implementazioni Windows Microsoft. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali.](security-considerations--international-features.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
