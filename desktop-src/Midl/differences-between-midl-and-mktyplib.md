---
title: Differenze tra MIDL e MkTypLib
description: Differenze tra MIDL e MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL e FAD MIDL, differenze tra MIDL e MkTypLib
- MIDL MkTypLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045355"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="20138-105">Differenze tra MIDL e MkTypLib</span><span class="sxs-lookup"><span data-stu-id="20138-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="20138-106">Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="20138-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="20138-107">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="20138-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="20138-108">Esistono alcune aree principali in cui il compilatore MIDL è diverso da MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="20138-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="20138-109">La maggior parte di queste differenze si verifica perché MIDL è orientato più verso la sintassi C rispetto a MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="20138-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="20138-110">In generale, è consigliabile usare la sintassi MIDL nei file IDL.</span><span class="sxs-lookup"><span data-stu-id="20138-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="20138-111">Tuttavia, se è necessario compilare un file FAD esistente o in caso contrario mantenere la compatibilità con MkTypLib, usare l'opzione del compilatore MIDL [**/mktyplib203**](-mktyplib203.md) per forzare il comportamento di midl come Mkktyplib.exe, versione 2,03.</span><span class="sxs-lookup"><span data-stu-id="20138-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="20138-112">(Si tratta dell'ultima versione dello strumento MkTypLib). In particolare, l'opzione **/mktyplib203** risolve le differenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="20138-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="20138-113">sintassi typedef per i tipi di dati complessi</span><span class="sxs-lookup"><span data-stu-id="20138-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="20138-114">In MkTypLib entrambe le definizioni seguenti generano un record TKIND \_ per "questo \_ struct" nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="20138-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="20138-115">Il tag "struct \_ tag" è facoltativo e, se usato, non verrà visualizzato nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="20138-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="20138-116">Se manca un tag facoltativo, MIDL lo genererà aggiungendo un tag alla definizione fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20138-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="20138-117">Poiché la prima definizione include un tag, MIDL genererà un \_ record TKIND per "questo \_ struct" e un \_ alias TKIND per "questo struct \_ " (definendo " \_ struct" come alias per "struct \_ tag").</span><span class="sxs-lookup"><span data-stu-id="20138-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="20138-118">Poiché il tag non è presente nella seconda definizione, MIDL genererà un \_ record TKIND per un nome modificato, interno a MIDL, che non è significativo per l'utente e un alias TKIND \_ per "tale \_ struct".</span><span class="sxs-lookup"><span data-stu-id="20138-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="20138-119">Ciò ha implicazioni potenziali per i browser della libreria dei tipi che visualizzano semplicemente il nome di un record nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="20138-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="20138-120">Se si prevede che un \_ record TKIND abbia un nome reale, nell'interfaccia utente potrebbero essere presenti nomi non riconoscibili.</span><span class="sxs-lookup"><span data-stu-id="20138-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="20138-121">Questo comportamento si applica anche alle definizioni di [**Union**](union.md) e [**enum**](enum.md) , con il compilatore MIDL che genera \_ rispettivamente le unioni TKIND e le \_ enumerazioni TKIND.</span><span class="sxs-lookup"><span data-stu-id="20138-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="20138-122">MIDL consente inoltre le definizioni di [**struct**](struct.md), [**Union**](union.md)e [**enum**](enum.md) di tipo C.</span><span class="sxs-lookup"><span data-stu-id="20138-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="20138-123">La definizione seguente, ad esempio, è valida in MIDL:</span><span class="sxs-lookup"><span data-stu-id="20138-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="20138-124">tipi di dati Boolean</span><span class="sxs-lookup"><span data-stu-id="20138-124">Boolean data types</span></span>

    <span data-ttu-id="20138-125">In MkTypLib, il tipo di base [**booleano**](boolean.md) e il tipo di dati MkTypLib bool corrispondono a VT \_ bool, che esegue il mapping a Variant \_ bool e che è definito come [**short**](short.md).</span><span class="sxs-lookup"><span data-stu-id="20138-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="20138-126">In MIDL il tipo di base **booleano** è equivalente a VT \_ Ui1, che è definito come [**unsigned char**](unsigned.md)e il tipo di dati bool è definito come [**Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="20138-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="20138-127">Ciò comporta difficoltà se si combinano la sintassi di IDL e la sintassi di gestione delle funzioni di gestione delle funzioni nello stesso file, cercando comunque di mantenere la compatibilità con MkTypLib.</span><span class="sxs-lookup"><span data-stu-id="20138-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="20138-128">Poiché i tipi di dati hanno dimensioni diverse, il codice di marshalling non corrisponderà a quanto descritto nelle informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="20138-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="20138-129">Se si desidera un valore \_ bool di VT nella libreria dei tipi, è necessario utilizzare il \_ tipo di dati bool Variant.</span><span class="sxs-lookup"><span data-stu-id="20138-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="20138-130">Definizioni GUID nei file di intestazione</span><span class="sxs-lookup"><span data-stu-id="20138-130">GUID definitions in header files</span></span>

    <span data-ttu-id="20138-131">In MkTypLib i GUID vengono definiti nel file di intestazione con una macro che può essere compilata in modo condizionale per generare una predefinizione GUID o un GUID di cui è stata creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="20138-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="20138-132">MIDL in genere inserisce le predefinizioni GUID nei file di intestazione e nelle creazioni GUID generate solo nel file generato dall'opzione [**/IID**](-iid.md) .</span><span class="sxs-lookup"><span data-stu-id="20138-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="20138-133">Le differenze di comportamento seguenti non possono essere risolte tramite l'opzione [**/mktyplib203**](-mktyplib203.md) :</span><span class="sxs-lookup"><span data-stu-id="20138-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="20138-134">Maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="20138-134">Case sensitivity</span></span>

    <span data-ttu-id="20138-135">MIDL fa distinzione tra maiuscole e minuscole. l'automazione OLE non lo è.</span><span class="sxs-lookup"><span data-stu-id="20138-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="20138-136">Ambito dei simboli in una dichiarazione di enumerazione</span><span class="sxs-lookup"><span data-stu-id="20138-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="20138-137">In MkTypLib l'ambito dei simboli in un'enumerazione è local.</span><span class="sxs-lookup"><span data-stu-id="20138-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="20138-138">In MIDL l'ambito dei simboli in un'enumerazione è globale, così com'è in C. Il codice seguente, ad esempio, verrà compilato in MkTypLib, ma genererà un errore di nome duplicato in MIDL:</span><span class="sxs-lookup"><span data-stu-id="20138-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="20138-139">Ambito dell'attributo pubblico</span><span class="sxs-lookup"><span data-stu-id="20138-139">Scope of public attribute</span></span>

    <span data-ttu-id="20138-140">Se si applica l'attributo [**public**](public.md) a un blocco di interfaccia, MkTypLib considera ogni typedef all'interno del blocco di interfaccia come Public.</span><span class="sxs-lookup"><span data-stu-id="20138-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="20138-141">MIDL richiede che l'attributo **public** venga applicato in modo esplicito ai typedef che si desidera public.</span><span class="sxs-lookup"><span data-stu-id="20138-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="20138-142">Ordine di ricerca importlib</span><span class="sxs-lookup"><span data-stu-id="20138-142">Importlib search order</span></span>

    <span data-ttu-id="20138-143">Se si importano più librerie dei tipi e se queste librerie contengono riferimenti duplicati, MkTypLib risolve questo problema utilizzando il primo riferimento rilevato.</span><span class="sxs-lookup"><span data-stu-id="20138-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="20138-144">MIDL utilizzerà l'ultimo riferimento rilevato.</span><span class="sxs-lookup"><span data-stu-id="20138-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="20138-145">Se, ad esempio, si utilizza la seguente sintassi per la funzione di ricerca per indicizzazione, la libreria C utilizzerà il typedef MOO dalla libreria A se si compila con MkTypLib e il typedef di MOO dalla libreria B se si compila con MIDL:</span><span class="sxs-lookup"><span data-stu-id="20138-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="20138-146">La soluzione alternativa appropriata per questa operazione consiste nel qualificare ogni riferimento con il nome corretto della libreria di importazione, come segue:</span><span class="sxs-lookup"><span data-stu-id="20138-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="20138-147">Tipo di dati VOID non riconosciuto</span><span class="sxs-lookup"><span data-stu-id="20138-147">VOID data type not recognized</span></span>

    <span data-ttu-id="20138-148">MIDL riconosce il tipo di dati [**void**](void.md) del linguaggio C e non riconosce il tipo di dati void di automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="20138-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="20138-149">Se si dispone di un file FAD che usa VOID, inserire questa definizione all'inizio del file:</span><span class="sxs-lookup"><span data-stu-id="20138-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="20138-150">Notazione esponenziale</span><span class="sxs-lookup"><span data-stu-id="20138-150">Exponential notation</span></span>

    <span data-ttu-id="20138-151">MIDL richiede che i valori espressi in notazione esponenziale siano contenuti tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="20138-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="20138-152">Ad esempio, "-2.5 E + 3"</span><span class="sxs-lookup"><span data-stu-id="20138-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="20138-153">Valori LCID e costanti</span><span class="sxs-lookup"><span data-stu-id="20138-153">LCID values and constants</span></span>

    <span data-ttu-id="20138-154">In genere MIDL non considera l'LCID durante l'analisi dei file.</span><span class="sxs-lookup"><span data-stu-id="20138-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="20138-155">Per forzare questo comportamento per un valore o se è necessario usare la notazione specifica delle impostazioni locali durante la definizione di una costante, racchiudere il valore o la costante tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="20138-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="20138-156">Per ulteriori informazioni, vedere [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)e [marshalling dei tipi di dati OLE](marshaling-ole-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="20138-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




