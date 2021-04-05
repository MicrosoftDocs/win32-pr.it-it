---
title: Considerazioni su Unicode
description: La funzione del servizio WriteFmtUserTypeStg, usata nel metodo Save di IPaper, richiede parametri stringa Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856174"
---
# <a name="unicode-considerations"></a>Considerazioni su Unicode

La funzione del servizio **WriteFmtUserTypeStg** , usata nel metodo [**iPaper:: Save**](ipaper--save.md) , richiede parametri stringa Unicode. Questo avviene con le chiamate al servizio COM/OLE che accettano parametri di stringa. Quando si esegue la compilazione per le stringhe ANSI, i parametri Unicode previsti richiedono la conversione da ANSI a Unicode. Questo processo viene eseguito usando alcune macro in APPUTIL. h che possono nascondere le conversioni. Vedere ad esempio **WriteFmtUserTypeStg**.

Nel metodo [**Save**](ipaper--save.md) viene visualizzata la chiamata seguente.


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Quando **StoServe** viene compilato per ANSI (non per Unicode), questa chiamata si riduce effettivamente a una chiamata a una funzione surrogata APPUTIL interna. Per supportare questa operazione, in apputil. h, che è un file incluso in tutti gli esempi di codice, viene usato lo schema macro seguente. File CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



Lo schema utilizza funzioni di chiamata del servizio surrogato. Le versioni ANSI delle chiamate iniziano con \_ . Queste funzioni ANSI surrogate sono implementate in apputil. cpp. Vengono usati quando l'esempio di codice viene compilato per le stringhe ANSI (impostazione predefinita nei makefile). Le funzioni di servizio che i surrogati sono in grado di supportare solo parametri stringa Unicode. Questa operazione impone alcune conversioni di stringa da ANSI a Unicode prima che venga effettuata la chiamata al servizio COM/OLE reale all'interno del surrogato.

Se, ad esempio, UNICODE non è definito durante la compilazione, tutte le chiamate negli esempi alla funzione del servizio com **WriteFmtUserTypeStg** vengono effettivamente modificate dalle macro in chiamate a una \_ funzione WriteFmtUserTypeStg implementata in APPUTIL. CPP. Questa funzione accetta il puntatore di stringa ANSI di input, lo converte in una copia Unicode e passa la copia Unicode come parametro di stringa in una chiamata alla funzione **WriteFmtUserTypeStg** effettiva.

Di seguito è riportato un \_ WriteFmtUserTypeStg di apputil. cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




