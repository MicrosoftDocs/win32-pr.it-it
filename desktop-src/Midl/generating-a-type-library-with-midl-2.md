---
title: Generazione di una libreria dei tipi con MIDL
description: L'elemento di livello principale della sintassi di FAD è l'istruzione Library (blocco libreria).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL, attività, generazione di una libreria di tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299804"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="b2aad-104">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="b2aad-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="b2aad-105">L'elemento di livello principale della sintassi di FAD è l'istruzione Library (blocco libreria).</span><span class="sxs-lookup"><span data-stu-id="b2aad-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="b2aad-106">Ogni altra istruzione, ad eccezione degli attributi applicati all'istruzione Library, deve essere definita all'interno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="b2aad-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="b2aad-107">Quando il compilatore MIDL rileva un blocco di libreria, genera una libreria dei tipi in modo analogo a quanto accade con MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="b2aad-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="b2aad-108">Con alcune eccezioni, descritte in [differenze tra MIDL e MkTypLib](differences-between-midl-and-mktyplib.md), le istruzioni all'interno del blocco di libreria devono seguire la stessa sintassi del linguaggio FAD e mktyplib.</span><span class="sxs-lookup"><span data-stu-id="b2aad-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="b2aad-109">Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="b2aad-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="b2aad-110">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b2aad-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="b2aad-111">È possibile applicare gli attributi di FAD agli elementi definiti all'interno o all'esterno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="b2aad-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="b2aad-112">Questi attributi non hanno alcun effetto all'esterno del blocco di libreria, a meno che all'elemento a cui viene applicato non venga fatto riferimento all'interno del blocco di libreria.</span><span class="sxs-lookup"><span data-stu-id="b2aad-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="b2aad-113">Le istruzioni all'interno del blocco di libreria possono fare riferimento a un elemento esterno utilizzandolo come tipo di base, ereditando da esso oppure facendo riferimento a una riga come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b2aad-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="b2aad-114">Se all'interno del blocco di libreria viene fatto riferimento a un elemento definito all'esterno del blocco di libreria, la relativa definizione verrà inserita nella libreria dei tipi generata.</span><span class="sxs-lookup"><span data-stu-id="b2aad-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="b2aad-115">Il compilatore MIDL considera le istruzioni all'esterno di un blocco di libreria come un tipico file IDL e analizza tali istruzioni come è sempre stato fatto.</span><span class="sxs-lookup"><span data-stu-id="b2aad-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="b2aad-116">In genere, ciò significa generare stub in linguaggio C per un'applicazione RPC.</span><span class="sxs-lookup"><span data-stu-id="b2aad-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="b2aad-117">Per ulteriori informazioni sulla sintassi generale per un file di FAD, vedere la [sintassi del file FAD](/previous-versions/windows/desktop/automat/odl-file-syntax).</span><span class="sxs-lookup"><span data-stu-id="b2aad-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 