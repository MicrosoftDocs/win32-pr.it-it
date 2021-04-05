---
title: Disabilitazione di STRICT
description: Per disabilitare il controllo RIGOROSo dei tipi, definire il nome del simbolo senza \_ strict. In Visual C/C++ è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando/DNO \_ strict come opzione del compilatore.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711977"
---
# <a name="disabling-strict"></a><span data-ttu-id="f8ce8-104">Disabilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="f8ce8-104">Disabling STRICT</span></span>

<span data-ttu-id="f8ce8-105">Per disabilitare il controllo **rigoroso** dei tipi, definire il nome del simbolo **senza \_ strict**.</span><span class="sxs-lookup"><span data-stu-id="f8ce8-105">To disable **STRICT** type checking, define the symbol name **NO\_STRICT**.</span></span> <span data-ttu-id="f8ce8-106">In Visual C/C++ è anche possibile specificare questa definizione nella riga di comando o in un makefile specificando **/dno \_ strict** come opzione del compilatore.</span><span class="sxs-lookup"><span data-stu-id="f8ce8-106">In Visual C/C++, you can also specify this definition on the command line or in a makefile by specifying **/DNO\_STRICT** as a compiler option.</span></span>

<span data-ttu-id="f8ce8-107">Per definire **Nessuna \_ restrizione** in base a file, inserire un'istruzione **\# define** prima di includere Windows. h:</span><span class="sxs-lookup"><span data-stu-id="f8ce8-107">To define **NO\_STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define NO_STRICT
#include <windows.h>
```



<span data-ttu-id="f8ce8-108">Per ottenere risultati ottimali, è necessario impostare anche il livello di avviso per i messaggi di errore su almeno **/W3**.</span><span class="sxs-lookup"><span data-stu-id="f8ce8-108">For best results, you should also set the warning level for error messages to at least **/W3**.</span></span> <span data-ttu-id="f8ce8-109">Questa operazione è sempre consigliabile con le applicazioni per Windows, perché una procedura di codifica che genera un avviso, ad esempio il passaggio di un numero errato di parametri, causa in genere un errore irreversibile in fase di esecuzione se non viene corretto.</span><span class="sxs-lookup"><span data-stu-id="f8ce8-109">This is always advisable with applications for Windows, because a coding practice that causes a warning (for example, passing the wrong number of parameters) usually causes a fatal error at run time if it is not corrected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8ce8-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8ce8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8ce8-111">Abilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="f8ce8-111">Enabling STRICT</span></span>](enabling-strict.md)
</dt> <dt>

[<span data-ttu-id="f8ce8-112">Conformità RIGOROSa</span><span class="sxs-lookup"><span data-stu-id="f8ce8-112">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 




