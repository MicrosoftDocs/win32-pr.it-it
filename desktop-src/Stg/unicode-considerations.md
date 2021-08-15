---
title: Considerazioni su Unicode
description: La funzione del servizio WriteFmtUserTypeStg, usata nel metodo IPaper Save, richiede parametri stringa Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06f8fa9592d3f29ccf82d42f38a48b2dc57d36bccf79b22b8fe159bad337cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886739"
---
# <a name="unicode-considerations"></a>Considerazioni su Unicode

La **funzione del servizio WriteFmtUserTypeStg,** usata nel metodo [**IPaper::Save,**](ipaper--save.md) richiede parametri di stringa Unicode. Questo è il caso delle chiamate al servizio COM/OLE che accettano parametri stringa. Quando si compilano stringhe ANSI, i parametri Unicode previsti devono essere conversioni da ANSI a Unicode. Questo processo viene ottenuto usando alcune macro in APPUTIL.h che potrebbero nascondere le conversioni. Ad esempio, vedere **WriteFmtUserTypeStg**.

La chiamata seguente viene visualizzata nel [**metodo Save.**](ipaper--save.md)


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Quando **StoServe viene** compilato per ANSI (non per Unicode), questa chiamata riduce effettivamente a una chiamata a una funzione surrogata APPUTIL interna. A tale scopo, in Apputil.h viene usato lo schema macro seguente, che è un file incluso in tutto l'esempio di codice . File CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



Lo schema usa funzioni di chiamata al servizio surrogate. Le versioni ANSI delle chiamate iniziano con \_ . Queste funzioni ANSI surrogate vengono implementate in Apputil.cpp. Vengono usati quando l'esempio di codice viene compilato per le stringhe ANSI (impostazione predefinita nei makefile). Le funzioni del servizio che i surrogati supportano solo parametri di stringa Unicode. In questo modo vengono forzate alcune conversioni di stringhe da ANSI a Unicode prima che venga eseguita la chiamata al servizio COM/OLE reale all'interno del surrogato.

Ad esempio, se UNICODE non è definito durante la compilazione, tutte le chiamate negli esempi alla funzione del servizio COM **WriteFmtUserTypeStg** vengono effettivamente modificate dalle macro in chiamate a una funzione \_ WriteFmtUserTypeStg implementata in APPUTIL. CPP. Questa funzione accetta il puntatore di stringa ANSI di input, lo converte in una copia Unicode e passa tale copia Unicode come parametro di stringa in una chiamata alla funzione **WriteFmtUserTypeStg** effettiva.

Ecco \_ WriteFmtUserTypeStg di Apputil.cpp.

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

 

 




