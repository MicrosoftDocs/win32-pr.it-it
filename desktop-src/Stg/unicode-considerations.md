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
# <a name="unicode-considerations"></a><span data-ttu-id="7e199-103">Considerazioni su Unicode</span><span class="sxs-lookup"><span data-stu-id="7e199-103">Unicode Considerations</span></span>

<span data-ttu-id="7e199-104">La funzione del servizio **WriteFmtUserTypeStg** , usata nel metodo [**iPaper:: Save**](ipaper--save.md) , richiede parametri stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e199-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="7e199-105">Questo avviene con le chiamate al servizio COM/OLE che accettano parametri di stringa.</span><span class="sxs-lookup"><span data-stu-id="7e199-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="7e199-106">Quando si esegue la compilazione per le stringhe ANSI, i parametri Unicode previsti richiedono la conversione da ANSI a Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e199-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="7e199-107">Questo processo viene eseguito usando alcune macro in APPUTIL. h che possono nascondere le conversioni.</span><span class="sxs-lookup"><span data-stu-id="7e199-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="7e199-108">Vedere ad esempio **WriteFmtUserTypeStg**.</span><span class="sxs-lookup"><span data-stu-id="7e199-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="7e199-109">Nel metodo [**Save**](ipaper--save.md) viene visualizzata la chiamata seguente.</span><span class="sxs-lookup"><span data-stu-id="7e199-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="7e199-110">Quando **StoServe** viene compilato per ANSI (non per Unicode), questa chiamata si riduce effettivamente a una chiamata a una funzione surrogata APPUTIL interna.</span><span class="sxs-lookup"><span data-stu-id="7e199-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="7e199-111">Per supportare questa operazione, in apputil. h, che è un file incluso in tutti gli esempi di codice, viene usato lo schema macro seguente. File CPP.</span><span class="sxs-lookup"><span data-stu-id="7e199-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="7e199-112">Lo schema utilizza funzioni di chiamata del servizio surrogato.</span><span class="sxs-lookup"><span data-stu-id="7e199-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="7e199-113">Le versioni ANSI delle chiamate iniziano con \_ .</span><span class="sxs-lookup"><span data-stu-id="7e199-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="7e199-114">Queste funzioni ANSI surrogate sono implementate in apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="7e199-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="7e199-115">Vengono usati quando l'esempio di codice viene compilato per le stringhe ANSI (impostazione predefinita nei makefile).</span><span class="sxs-lookup"><span data-stu-id="7e199-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="7e199-116">Le funzioni di servizio che i surrogati sono in grado di supportare solo parametri stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e199-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="7e199-117">Questa operazione impone alcune conversioni di stringa da ANSI a Unicode prima che venga effettuata la chiamata al servizio COM/OLE reale all'interno del surrogato.</span><span class="sxs-lookup"><span data-stu-id="7e199-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="7e199-118">Se, ad esempio, UNICODE non è definito durante la compilazione, tutte le chiamate negli esempi alla funzione del servizio com **WriteFmtUserTypeStg** vengono effettivamente modificate dalle macro in chiamate a una \_ funzione WriteFmtUserTypeStg implementata in APPUTIL. CPP.</span><span class="sxs-lookup"><span data-stu-id="7e199-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="7e199-119">Questa funzione accetta il puntatore di stringa ANSI di input, lo converte in una copia Unicode e passa la copia Unicode come parametro di stringa in una chiamata alla funzione **WriteFmtUserTypeStg** effettiva.</span><span class="sxs-lookup"><span data-stu-id="7e199-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="7e199-120">Di seguito è riportato un \_ WriteFmtUserTypeStg di apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="7e199-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




