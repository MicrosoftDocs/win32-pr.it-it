---
title: Stringhe (RPC)
description: Tre tipi di stringhe e RPC (Remote Procedure Call).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338710"
---
# <a name="strings-rpc"></a><span data-ttu-id="39d0c-103">Stringhe (RPC)</span><span class="sxs-lookup"><span data-stu-id="39d0c-103">Strings (RPC)</span></span>

<span data-ttu-id="39d0c-104">Sono disponibili tre tipi di stringhe denotate dalle seguenti sottostringhe finali nel formato carattere.</span><span class="sxs-lookup"><span data-stu-id="39d0c-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="39d0c-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="39d0c-105">Type</span></span>                  | <span data-ttu-id="39d0c-106">Substring</span><span class="sxs-lookup"><span data-stu-id="39d0c-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="39d0c-107">Stringa di caratteri</span><span class="sxs-lookup"><span data-stu-id="39d0c-107">Character string</span></span>      | <span data-ttu-id="39d0c-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="39d0c-108">CSTRING</span></span>   |
| <span data-ttu-id="39d0c-109">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="39d0c-109">Wide character string</span></span> | <span data-ttu-id="39d0c-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="39d0c-110">WSTRING</span></span>   |
| <span data-ttu-id="39d0c-111">Struttura in grado di String</span><span class="sxs-lookup"><span data-stu-id="39d0c-111">String-able structure</span></span> | <span data-ttu-id="39d0c-112">SSTRING</span><span class="sxs-lookup"><span data-stu-id="39d0c-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="39d0c-113">Stringhe non conformi</span><span class="sxs-lookup"><span data-stu-id="39d0c-113">Nonconformant Strings</span></span>

<span data-ttu-id="39d0c-114">Un esempio di stringa non conforme è una **\[ stringa \]** in una matrice di dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="39d0c-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="39d0c-115">Stringhe conformi</span><span class="sxs-lookup"><span data-stu-id="39d0c-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="39d0c-116">–oppure–</span><span class="sxs-lookup"><span data-stu-id="39d0c-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="39d0c-117">Il primo formato descrive stringhe comuni, come un argomento di tipo **\[ \] stringa** char \* .</span><span class="sxs-lookup"><span data-stu-id="39d0c-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="39d0c-118">Una stringa conforme alle dimensioni ha la seconda descrizione.</span><span class="sxs-lookup"><span data-stu-id="39d0c-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="39d0c-119">La descrizione della conformità \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="39d0c-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="39d0c-120">Stringhe di struttura</span><span class="sxs-lookup"><span data-stu-id="39d0c-120">Structure Strings</span></span>

<span data-ttu-id="39d0c-121">Di seguito è riportata una struttura non conforme in grado di String:</span><span class="sxs-lookup"><span data-stu-id="39d0c-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="39d0c-122">Struttura conforme alle stringhe:</span><span class="sxs-lookup"><span data-stu-id="39d0c-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="39d0c-123">o</span><span class="sxs-lookup"><span data-stu-id="39d0c-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="39d0c-124">La seconda descrizione è relativa a una struttura di dimensioni in grado di consentire la stringa.</span><span class="sxs-lookup"><span data-stu-id="39d0c-124">The latter description is for a sized string-able structure.</span></span>

 

 