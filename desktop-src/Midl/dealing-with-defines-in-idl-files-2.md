---
title: Gestione delle definizioni nei file IDL
description: Questa pagina descrive il motivo per cui i simboli definiti con un \ define scompaiono dal compilatore MIDL che ha generato i file H e cosa può essere fatto. Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio i file \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL compilatore MIDL, gestione delle definizioni
- definisce MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044670"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="c8d07-106">Gestione delle \# definizioni nei file IDL</span><span class="sxs-lookup"><span data-stu-id="c8d07-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="c8d07-107">Questa pagina descrive il motivo per cui i simboli definiti con una **\# definizione** scompaiono dal compilatore MIDL che genera file H e cosa può essere fatto.</span><span class="sxs-lookup"><span data-stu-id="c8d07-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="c8d07-108">Questa spiegazione si applica a tutti i file elaborati da MIDL, ad esempio \* i file con estensione IDL, \* ACF e \* h.</span><span class="sxs-lookup"><span data-stu-id="c8d07-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="c8d07-109">La scomparsa dei simboli **\# define** è il risultato della delega della pre-elaborazione dei file di input a un preprocessore.</span><span class="sxs-lookup"><span data-stu-id="c8d07-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="c8d07-110">Per impostazione predefinita, il preprocessore è un preprocessore C/C++ dall'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="c8d07-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="c8d07-111">Dopo la pre-elaborazione, il flusso di input MIDL receives ha solo \# direttive per il preprocessore line.</span><span class="sxs-lookup"><span data-stu-id="c8d07-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="c8d07-112">In particolare, il preprocessore esegue la registrazione di tutte le definizioni di macro nei file di input e, di conseguenza, MIDL non è in grado di rilevare la loro presenza.</span><span class="sxs-lookup"><span data-stu-id="c8d07-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="c8d07-113">Di conseguenza, quando MIDL replica le definizioni dei tipi da un file di input al file H generato, le definizioni \# non vengono replicate.</span><span class="sxs-lookup"><span data-stu-id="c8d07-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="c8d07-114">Pertanto, non utilizzare \# le definizioni direttamente nei file idl se devono essere utilizzate in un secondo momento dal file H generato.</span><span class="sxs-lookup"><span data-stu-id="c8d07-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="c8d07-115">Sono consigliate le quattro soluzioni alternative seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8d07-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="c8d07-116">Usare la specifica di Dichiarazione [**const**](const.md) .</span><span class="sxs-lookup"><span data-stu-id="c8d07-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="c8d07-117">Usare file di intestazione separati che vengono importati o inclusi nel file IDL e successivamente inclusi nel codice sorgente C.</span><span class="sxs-lookup"><span data-stu-id="c8d07-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="c8d07-118">Utilizzare le costanti di enumerazione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="c8d07-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="c8d07-119">Usare [**la \_ virgoletta cpp**](cpp-quote.md) per riprodurre la **\# definizione** nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="c8d07-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="c8d07-120">È possibile riprodurre le costanti manifesto usando la **sintassi della dichiarazione di costanti IDL**.</span><span class="sxs-lookup"><span data-stu-id="c8d07-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="c8d07-121">Si noti che il [**const**](const.md) nella dichiarazione di costante IDL è diverso dalla semantica **const** C/C++ e introduce semplicemente una costante denominata per una compilazione IDL.</span><span class="sxs-lookup"><span data-stu-id="c8d07-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="c8d07-122">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c8d07-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="c8d07-123">Questo esempio specifica che **ARRSIZE** è una costante con valore 10.</span><span class="sxs-lookup"><span data-stu-id="c8d07-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="c8d07-124">Le costanti denominate possono essere usate nei dichiaratori di matrici IDL e in altre posizioni in cui un programmatore C userà un manifesto definito.</span><span class="sxs-lookup"><span data-stu-id="c8d07-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="c8d07-125">Questa sintassi comporta inoltre la generazione della riga seguente nel file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="c8d07-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="c8d07-126">Un altro modo per gestire **\#** le istruzioni define consiste nel creare un pacchetto in un file di intestazione separato, in un file dedicato per la **\#** definizione di istruzioni o in un file che contiene solo definizioni di tipi.</span><span class="sxs-lookup"><span data-stu-id="c8d07-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="c8d07-127">Un file che contiene solo le direttive per il preprocessore può essere incluso in modo sicuro sia dal file IDL che dai file di origine C.</span><span class="sxs-lookup"><span data-stu-id="c8d07-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="c8d07-128">Sebbene le direttive non saranno disponibili nel file di intestazione generato dal compilatore MIDL, il programma C-Source può includere il file di intestazione separato.</span><span class="sxs-lookup"><span data-stu-id="c8d07-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="c8d07-129">Analogamente, un file di intestazione con **\#** istruzioni define e definizioni di tipo regolare può essere importato dal file IDL.</span><span class="sxs-lookup"><span data-stu-id="c8d07-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="c8d07-130">Questo approccio incapsula le **\#** istruzioni define e typedef usandole in un file H in modo che i **\#** simboli define non vengano usati direttamente nel file IDL di importazione.</span><span class="sxs-lookup"><span data-stu-id="c8d07-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="c8d07-131">L'importazione di un'intestazione o di un file IDL in un altro file IDL impedisce che le istruzioni typedef vengano replicate nel file H generato da MIDL (a differenza delle **\#** istruzioni di inclusione).</span><span class="sxs-lookup"><span data-stu-id="c8d07-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="c8d07-132">Questo approccio consente al file di intestazione originale di farvi riferimento in modo sicuro dal codice C lungo il file H generato senza problemi con le definizioni duplicate.</span><span class="sxs-lookup"><span data-stu-id="c8d07-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="c8d07-133">Anche l'utilizzo di costanti di enumerazione nel file IDL è efficace.</span><span class="sxs-lookup"><span data-stu-id="c8d07-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="c8d07-134">Queste costanti possono essere utilizzate nelle espressioni costanti in IDL, ad esempio nei dichiaratori di matrice.</span><span class="sxs-lookup"><span data-stu-id="c8d07-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="c8d07-135">Le costanti di enumerazione non vengono rimosse durante le fasi iniziali della compilazione MIDL da parte del preprocessore del compilatore C, quindi le costanti di enumerazione sono disponibili nel file di intestazione generato dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="c8d07-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="c8d07-136">Si consideri la seguente istruzione:</span><span class="sxs-lookup"><span data-stu-id="c8d07-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="c8d07-137">Questa istruzione non verrà rimossa durante la compilazione MIDL da parte del preprocessore C e il typedef verrà replicato nel file H generato.</span><span class="sxs-lookup"><span data-stu-id="c8d07-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="c8d07-138">La costante MAXSTRINGCOUNT è disponibile per i programmi di origine C che includono il file di intestazione generato dal compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="c8d07-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="c8d07-139">Infine, è possibile usare la direttiva per le [**\_ virgolette cpp**](cpp-quote.md) di MIDL per scrivere una stringa arbitraria direttamente nel file H generato.</span><span class="sxs-lookup"><span data-stu-id="c8d07-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="c8d07-140">Per ottenere, ad esempio, la costante del manifesto utilizzata in precedenza in questa pagina con **\_ virgolette cpp**, è possibile utilizzare l'istruzione seguente:</span><span class="sxs-lookup"><span data-stu-id="c8d07-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="c8d07-141">Questa istruzione determina la generazione della riga seguente nel file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="c8d07-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 




