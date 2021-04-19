---
title: Definizioni dei tipi, creazione di dichiarazioni e importazioni
description: Le definizioni dei tipi, le dichiarazioni di costrutto e le importazioni possono essere eseguite all'esterno del corpo dell'interfaccia.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfacce MIDL, definizioni di tipi
- interfacce MIDL, costrutti di dichiarazioni
- interfacce MIDL, Imports
- definizioni dei tipi MIDL
- costruire dichiarazioni MIDL
- Importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297911"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="99498-109">Definizioni dei tipi, creazione di dichiarazioni e importazioni</span><span class="sxs-lookup"><span data-stu-id="99498-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="99498-110">Le definizioni dei tipi, le dichiarazioni di costrutto e le importazioni possono essere eseguite all'esterno del corpo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99498-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="99498-111">Tutte le definizioni del file IDL principale verranno visualizzate nel file di intestazione generato e tutte le procedure di tutte le interfacce del file IDL principale genereranno routine stub.</span><span class="sxs-lookup"><span data-stu-id="99498-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="99498-112">Ciò consente alle applicazioni che supportano più interfacce di unire file IDL in un unico file IDL combinato.</span><span class="sxs-lookup"><span data-stu-id="99498-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="99498-113">Di conseguenza, richiede meno tempo per la compilazione dei file e consente anche a MIDL di ridurre le ridondanze negli stub generati.</span><span class="sxs-lookup"><span data-stu-id="99498-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="99498-114">Questo può migliorare significativamente le interfacce degli [**oggetti**](object.md) attraverso la possibilità di condividere codice comune per interfacce di base e interfacce derivate.</span><span class="sxs-lookup"><span data-stu-id="99498-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="99498-115">Per le interfacce non **oggetto** , i nomi delle procedure devono essere univoci in tutte le interfacce.</span><span class="sxs-lookup"><span data-stu-id="99498-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="99498-116">Per le interfacce di **oggetti** , i nomi delle procedure devono essere univoci solo all'interno di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99498-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="99498-117">Si noti che non sono consentite più interfacce quando si usa l'opzione [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="99498-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="99498-118">Costrutti dichiarativi</span><span class="sxs-lookup"><span data-stu-id="99498-118">Declarative Constructs</span></span>

<span data-ttu-id="99498-119">La sintassi per i costrutti dichiarativi nel file IDL è simile a quella per C. MIDL supporta tutti i costrutti dichiarativi di Microsoft C/C++ tranne i seguenti:</span><span class="sxs-lookup"><span data-stu-id="99498-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="99498-120">Dichiaratori di stile precedenti che consentono di specificare un dichiaratore senza un identificatore di tipo, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="99498-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="99498-121">Dichiarazioni con inizializzatori (MIDL accetta solo le dichiarazioni conformi alla sintassi di MIDL [**const**](const.md) ).</span><span class="sxs-lookup"><span data-stu-id="99498-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="99498-122">La parola chiave [**Import**](import.md) specifica i nomi di uno o più file IDL da importare.</span><span class="sxs-lookup"><span data-stu-id="99498-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="99498-123">La direttiva import è simile alla direttiva C [**include**](include.md) , ad eccezione del fatto che solo i tipi di dati vengono incorporati nel file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="99498-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="99498-124">Dichiarazione di costante</span><span class="sxs-lookup"><span data-stu-id="99498-124">Constant Declaration</span></span>

<span data-ttu-id="99498-125">La dichiarazione di costante specifica le costanti [**booleane**](boolean.md), Integer, character, wide character, String **e \* void** .</span><span class="sxs-lookup"><span data-stu-id="99498-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="99498-126">Per ulteriori informazioni, vedere [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="99498-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="99498-127">Dichiarazione generale</span><span class="sxs-lookup"><span data-stu-id="99498-127">General Declaration</span></span>

<span data-ttu-id="99498-128">Una dichiarazione generale è simile all'istruzione C [**typedef**](typedef.md) con l'aggiunta di attributi di tipo IDL.</span><span class="sxs-lookup"><span data-stu-id="99498-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="99498-129">Fatta eccezione per la modalità [**/OSF**](-osf.md) , il compilatore MIDL consente anche una dichiarazione implicita sotto forma di definizione di variabile.</span><span class="sxs-lookup"><span data-stu-id="99498-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="99498-130">Dichiarazione di funzione</span><span class="sxs-lookup"><span data-stu-id="99498-130">Function Declaration</span></span>

<span data-ttu-id="99498-131">Il dichiaratore di funzione è un caso speciale della dichiarazione generale.</span><span class="sxs-lookup"><span data-stu-id="99498-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="99498-132">È possibile utilizzare gli attributi IDL per specificare il comportamento del tipo restituito della funzione e di ognuno dei parametri.</span><span class="sxs-lookup"><span data-stu-id="99498-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="99498-133">Esempi</span><span class="sxs-lookup"><span data-stu-id="99498-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




