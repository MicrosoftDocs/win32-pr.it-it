---
description: Le librerie di runtime C standard contengono entrambe le versioni Unicode UTF-16 (carattere wide) delle funzioni stringa che è possibile usare con le versioni Unicode e orientata ai byte delle funzioni stringa che possono essere usate con i caratteri dei set di caratteri a byte singolo (SBCSs). Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar \_ t in ANSI C e consente l'accesso alle funzioni stringa Unicode. Le versioni Unicode delle funzioni iniziano con le lettere &\# 0034; wcs&\# 0034; (o a volte &\# 0034; \_ WCS&\# 0034;). Il tipo di dati CHAR utilizzato per le tabelle codici è compatibile con il tipo di dati carattere char in ANSI C, per consentire l'accesso alle funzioni per le stringhe di caratteri. Le versioni dei caratteri delle funzioni iniziano con le lettere &\# 0034; str&\# 0034;. Sono inoltre disponibili versioni speciali per i set di caratteri a doppio byte (DBCS) che iniziano con le lettere &\# 0034; \_ MB&\# 0034;.
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: Funzioni C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885549"
---
# <a name="standard-c-functions"></a>Funzioni C standard

Le librerie di runtime C standard contengono entrambe le versioni Unicode UTF-16 (carattere wide) delle funzioni stringa che è possibile usare con le versioni [Unicode](unicode.md) e orientata ai byte delle funzioni stringa che possono essere usate con i caratteri dei [set di caratteri a byte singolo](single-byte-character-sets.md) (SBCSs). Il tipo di dati Unicode WCHAR è compatibile con il tipo di dati wchar \_ t in ANSI C e consente l'accesso alle funzioni stringa Unicode. Le versioni Unicode delle funzioni iniziano con le lettere "WCS" (o a volte " \_ WCS"). Il tipo di dati CHAR utilizzato per le tabelle codici è compatibile con il tipo di dati carattere char in ANSI C, per consentire l'accesso alle funzioni per le stringhe di caratteri. Le versioni dei caratteri delle funzioni iniziano con le lettere "Str". Sono inoltre disponibili versioni speciali per i [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) che iniziano con le lettere " \_ MBS".

Le librerie di runtime C standard includono funzioni generiche per tutte le funzioni stringa C standard. Iniziano con " \_ TCS" e sono elencati nel file di intestazione Tchar. h. Queste funzioni usano il tipo di dati TCHAR generico.

Un'applicazione deve aggiungere le righe seguenti per usare le funzioni generiche e compilare per Unicode.


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



Si noti che sono necessari entrambi i file Tchar. h e WCHAR. h e che è necessario anche il carattere di sottolineatura principale della \_ variabile Unicode. Questa nomenclatura è specifica della libreria C standard. Il rendering "UNICODE" senza il carattere di sottolineatura è relativo ai runtime di Microsoft Windows.

Le funzioni [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) e [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) possono essere convertite dal set di caratteri supportato dalla libreria C standard in Unicode e viceversa, con alcune limitazioni. Per ulteriori informazioni sulla conversione di stringhe da e verso Unicode, vedere [conversione tra tipi di stringa](translation-between-string-types.md).

La funzione [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) definita in TCHAR. h supporta le stesse specifiche di formato delle funzioni di stampa strsafe. h, ad esempio [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa). Analogamente, TCHAR. h definisce una funzione [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) , in cui la stringa di formato è una stringa Unicode.

> [!Caution]  
> Una gestione dei buffer insufficiente è coinvolta in molti problemi di sicurezza che coinvolgono sovraccarichi del buffer. Vedere le informazioni di [riferimento su strsafe. h](../menurc/strsafe-ovw.md). Le funzioni definite in strsafe. h forniscono un'elaborazione aggiuntiva per la gestione appropriata del buffer nel codice. Hanno lo scopo di sostituire le controparti C/C++ predefinite, nonché le implementazioni specifiche di Microsoft Windows. Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
