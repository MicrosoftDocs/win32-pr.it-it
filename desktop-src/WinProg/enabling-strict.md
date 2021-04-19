---
title: Abilitazione di STRICT
description: Quando si definisce il simbolo STRICT, si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'utilizzo dei tipi.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320251"
---
# <a name="enabling-strict"></a><span data-ttu-id="2361f-103">Abilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="2361f-103">Enabling STRICT</span></span>

<span data-ttu-id="2361f-104">Quando si definisce il simbolo **strict** , si abilitano le funzionalità che richiedono maggiore attenzione nella dichiarazione e nell'utilizzo dei tipi.</span><span class="sxs-lookup"><span data-stu-id="2361f-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="2361f-105">Questo consente di scrivere codice più portatile.</span><span class="sxs-lookup"><span data-stu-id="2361f-105">This helps you write more portable code.</span></span> <span data-ttu-id="2361f-106">Questa ulteriore attenzione ridurrà anche il tempo di debug.</span><span class="sxs-lookup"><span data-stu-id="2361f-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="2361f-107">L'abilitazione di **strict** ridefinisce determinati tipi di dati in modo che il compilatore non consenta l'assegnazione da un tipo a un altro senza un cast esplicito.</span><span class="sxs-lookup"><span data-stu-id="2361f-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="2361f-108">Questa operazione è particolarmente utile per il codice di Windows.</span><span class="sxs-lookup"><span data-stu-id="2361f-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="2361f-109">Gli errori nel passaggio dei tipi di dati vengono segnalati in fase di compilazione anziché causare errori irreversibili in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2361f-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="2361f-110">Con Visual C++, il controllo dei tipi **strict** è definito per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2361f-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="2361f-111">Per definire **strict** in base a file, inserire un'istruzione **\# define** prima di includere Windows. h:</span><span class="sxs-lookup"><span data-stu-id="2361f-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="2361f-112">Quando è definito **strict** , le definizioni [dei tipi di dati](windows-data-types.md) cambiano come segue:</span><span class="sxs-lookup"><span data-stu-id="2361f-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="2361f-113">I tipi di handle specifici vengono definiti per escludersi a vicenda. ad esempio, non sarà possibile passare un **HWND** in cui è richiesto un argomento di tipo **HDC** .</span><span class="sxs-lookup"><span data-stu-id="2361f-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="2361f-114">Senza **strict**, tutti gli handle sono definiti come **handle**, pertanto il compilatore non impedisce l'uso di un tipo di handle in cui è previsto un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="2361f-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="2361f-115">Tutti i tipi di funzione di callback, ad esempio le routine della finestra di dialogo, le routine della finestra e le routine hook, sono definiti con prototipi completi.</span><span class="sxs-lookup"><span data-stu-id="2361f-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="2361f-116">In questo modo si impedisce la dichiarazione di funzioni di callback con elenchi di parametri non corretti.</span><span class="sxs-lookup"><span data-stu-id="2361f-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="2361f-117">I tipi di parametro e valore restituito che devono usare un puntatore generico sono dichiarati correttamente come **LPVOID** anziché come **LPSTR** o un altro tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="2361f-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="2361f-118">La struttura [**Comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) viene dichiarata in base allo standard ANSI.</span><span class="sxs-lookup"><span data-stu-id="2361f-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2361f-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2361f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2361f-120">Disabilitazione di STRICT</span><span class="sxs-lookup"><span data-stu-id="2361f-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="2361f-121">Conformità RIGOROSa</span><span class="sxs-lookup"><span data-stu-id="2361f-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
