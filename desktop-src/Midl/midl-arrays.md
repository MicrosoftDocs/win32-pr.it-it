---
title: Matrici MIDL
description: Matrici MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipi di dati MIDL, matrici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046689"
---
# <a name="midl-arrays"></a><span data-ttu-id="4cde4-104">Matrici MIDL</span><span class="sxs-lookup"><span data-stu-id="4cde4-104">MIDL Arrays</span></span>

<span data-ttu-id="4cde4-105">I dichiaratori di matrice vengono visualizzati nel corpo dell'interfaccia del file IDL come uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="4cde4-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="4cde4-106">Parte di una dichiarazione generale</span><span class="sxs-lookup"><span data-stu-id="4cde4-106">Part of a general declaration</span></span>
-   <span data-ttu-id="4cde4-107">Membro di un dichiaratore di struttura o di Unione</span><span class="sxs-lookup"><span data-stu-id="4cde4-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="4cde4-108">Un parametro per una chiamata di procedura remota</span><span class="sxs-lookup"><span data-stu-id="4cde4-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="4cde4-109">I limiti di ogni dimensione della matrice sono espressi all'interno di una coppia separata di parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="4cde4-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="4cde4-110">Un'espressione che restituisce *n* indica un limite inferiore pari a zero e un limite superiore di *n-1*.</span><span class="sxs-lookup"><span data-stu-id="4cde4-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="4cde4-111">Se le parentesi quadre sono vuote o contengono un singolo asterisco ( \* ), il limite inferiore è zero e il limite superiore viene determinato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="4cde4-112">La matrice può inoltre contenere due valori separati da puntini di sospensione che rappresentano i limiti inferiore e superiore della matrice, come in \[ *basso*... *superiore* \] .</span><span class="sxs-lookup"><span data-stu-id="4cde4-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="4cde4-113">Microsoft RPC richiede un limite inferiore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="4cde4-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="4cde4-114">Il compilatore MIDL non riconosce i costrutti che specificano limiti inferiori diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="4cde4-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="4cde4-115">Le matrici possono essere associate alle dimensioni degli attributi del campo, mentre [**Max \_ è**](max-is.md), [**length \_ è**](length-is.md), [**First \_ è**](first-is.md)e [**Last \_**](last-is.md) consente di specificare la dimensione della matrice o la parte della matrice che contiene dati validi. [**\_**](size-is.md)</span><span class="sxs-lookup"><span data-stu-id="4cde4-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="4cde4-116">Questi attributi di campo identificano il parametro, il campo della struttura o la costante che specifica la dimensione o l'indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="4cde4-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="4cde4-117">La matrice deve essere associata all'identificatore specificato dall'attributo field nel modo seguente: quando la matrice è un parametro, l'identificatore deve essere anche un parametro per la stessa funzione. Quando la matrice è un campo della struttura, l'identificatore deve essere un altro campo struttura della stessa struttura.</span><span class="sxs-lookup"><span data-stu-id="4cde4-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="4cde4-118">Una matrice viene chiamata "conforme" Se il limite superiore di una dimensione viene determinato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="4cde4-119">Solo i limiti superiori possono essere determinati in fase di esecuzione. Per determinare il limite superiore, la dichiarazione di matrice deve includere [**una \_ dimensione**](size-is.md) oppure il valore [**massimo \_ è**](max-is.md) attributo.</span><span class="sxs-lookup"><span data-stu-id="4cde4-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="4cde4-120">Una matrice viene chiamata "varying" quando i relativi limiti vengono determinati in fase di compilazione, ma l'intervallo di elementi trasmessi viene determinato in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="4cde4-121">Per determinare l'intervallo di elementi trasmessi, la dichiarazione di matrice deve includere [**una \_ lunghezza**](length-is.md), ovvero il [**primo \_ è**](first-is.md)o [**l'ultimo \_**](last-is.md) attributo.</span><span class="sxs-lookup"><span data-stu-id="4cde4-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="4cde4-122">Una matrice di variabili conformi (detta anche "Open") è una matrice il cui limite superiore e l'intervallo di elementi trasmessi vengono determinati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="4cde4-123">Al massimo, una matrice di variabili conforme o conforme può essere annidata in una struttura C e deve essere l'ultimo elemento della struttura.</span><span class="sxs-lookup"><span data-stu-id="4cde4-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="4cde4-124">Al contrario, le matrici variabili non conformi possono essere presenti in qualsiasi punto di una struttura.</span><span class="sxs-lookup"><span data-stu-id="4cde4-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="4cde4-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="4cde4-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="4cde4-126">Per altre informazioni, vedere [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4cde4-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="4cde4-127">Matrici multidimensionali</span><span class="sxs-lookup"><span data-stu-id="4cde4-127">Multidimensional Arrays</span></span>

<span data-ttu-id="4cde4-128">L'utente può dichiarare tipi che sono matrici e quindi dichiarare matrici di oggetti di tali tipi.</span><span class="sxs-lookup"><span data-stu-id="4cde4-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="4cde4-129">La semantica delle matrici *m*-dimensionali dei tipi di matrici a *n* dimensioni corrisponde alla semantica delle  + matrici *n*-dimensionali m.</span><span class="sxs-lookup"><span data-stu-id="4cde4-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="4cde4-130">Il tipo RECT, ad esempio, \_ può essere definito come matrice bidimensionale e la variabile *Rect* può essere definita come una matrice di \_ tipo Rect.</span><span class="sxs-lookup"><span data-stu-id="4cde4-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="4cde4-131">Equivale alla matrice tridimensionale *equivalente a \_ Rect*:</span><span class="sxs-lookup"><span data-stu-id="4cde4-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="4cde4-132">Microsoft RPC è orientato a C.</span><span class="sxs-lookup"><span data-stu-id="4cde4-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="4cde4-133">Secondo le convenzioni del linguaggio C, solo la prima dimensione di una matrice multidimensionale può essere determinata in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="4cde4-134">L'interazione con le matrici IDL DCE che supportano altri linguaggi è limitata a:</span><span class="sxs-lookup"><span data-stu-id="4cde4-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="4cde4-135">Matrici multidimensionali con limiti costanti (in fase di compilazione).</span><span class="sxs-lookup"><span data-stu-id="4cde4-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="4cde4-136">Matrici multidimensionali con tutti i limiti costanti eccetto la prima dimensione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="4cde4-137">Il limite superiore e l'intervallo di elementi trasmessi della prima dimensione dipendono dal runtime.</span><span class="sxs-lookup"><span data-stu-id="4cde4-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="4cde4-138">Qualsiasi matrice unidimensionale con limite inferiore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="4cde4-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="4cde4-139">Quando l' **\[** [](string.md) **\]** attributo stringa viene utilizzato nelle matrici multidimensionali, l'attributo si applica alla matrice più a destra.</span><span class="sxs-lookup"><span data-stu-id="4cde4-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="4cde4-140">Matrici di puntatori</span><span class="sxs-lookup"><span data-stu-id="4cde4-140">Arrays of Pointers</span></span>

<span data-ttu-id="4cde4-141">I puntatori di riferimento devono puntare a dati validi.</span><span class="sxs-lookup"><span data-stu-id="4cde4-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="4cde4-142">L'applicazione client deve allocare tutta la memoria per un oggetto o in una **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** matrice di puntatori di riferimento, soprattutto quando la matrice è associata a **\[ in \]**, o **\[** **in \] , out**, **\[** [**length \_ is**](length-is.md) **\]** o **\[** [**Last \_ è**](last-is.md) **\]** values.</span><span class="sxs-lookup"><span data-stu-id="4cde4-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="4cde4-143">L'applicazione client deve anche inizializzare tutti gli elementi della matrice prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="4cde4-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="4cde4-144">Prima di tornare al client, l'applicazione server deve verificare che tutti gli elementi della matrice nell'intervallo trasmesso puntino a un archivio valido.</span><span class="sxs-lookup"><span data-stu-id="4cde4-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="4cde4-145">Sul lato server, lo stub alloca spazio di archiviazione per tutti gli elementi della matrice, indipendentemente dalla **\[** [**lunghezza \_**](length-is.md) **\]** o dall' **\[** [**ultimo \_**](last-is.md) **\]** valore al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="4cde4-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="4cde4-146">Questa funzionalità può influire sulle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4cde4-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="4cde4-147">Nessuna restrizione viene posizionata sulle matrici di puntatori univoci.</span><span class="sxs-lookup"><span data-stu-id="4cde4-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="4cde4-148">Nel client e nel server, lo spazio di archiviazione viene allocato per i puntatori null.</span><span class="sxs-lookup"><span data-stu-id="4cde4-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="4cde4-149">Quando i puntatori sono non null, i dati vengono inseriti in un'archiviazione preallocata.</span><span class="sxs-lookup"><span data-stu-id="4cde4-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="4cde4-150">Un dichiaratore di puntatore facoltativo può precedere il dichiaratore di matrice.</span><span class="sxs-lookup"><span data-stu-id="4cde4-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="4cde4-151">Quando i puntatori di riferimento incorporati sono **\[** [](out-idl.md) **\]** parametri di sola uscita, il codice server-Manager deve assegnare valori validi alla matrice di puntatori di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4cde4-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="4cde4-152">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4cde4-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="4cde4-153">Gli stub generati allocano la matrice e assegnano valori null a tutti i puntatori incorporati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4cde4-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 