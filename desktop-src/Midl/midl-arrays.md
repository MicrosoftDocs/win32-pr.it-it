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
# <a name="midl-arrays"></a>Matrici MIDL

I dichiaratori di matrice vengono visualizzati nel corpo dell'interfaccia del file IDL come uno dei seguenti:

-   Parte di una dichiarazione generale
-   Membro di un dichiaratore di struttura o di Unione
-   Un parametro per una chiamata di procedura remota

I limiti di ogni dimensione della matrice sono espressi all'interno di una coppia separata di parentesi quadre. Un'espressione che restituisce *n* indica un limite inferiore pari a zero e un limite superiore di *n-1*. Se le parentesi quadre sono vuote o contengono un singolo asterisco ( \* ), il limite inferiore è zero e il limite superiore viene determinato in fase di esecuzione.

La matrice può inoltre contenere due valori separati da puntini di sospensione che rappresentano i limiti inferiore e superiore della matrice, come in \[ *basso*... *superiore* \] . Microsoft RPC richiede un limite inferiore pari a zero. Il compilatore MIDL non riconosce i costrutti che specificano limiti inferiori diversi da zero.

Le matrici possono essere associate alle dimensioni degli attributi del campo, mentre [**Max \_ è**](max-is.md), [**length \_ è**](length-is.md), [**First \_ è**](first-is.md)e [**Last \_**](last-is.md) consente di specificare la dimensione della matrice o la parte della matrice che contiene dati validi. [**\_**](size-is.md) Questi attributi di campo identificano il parametro, il campo della struttura o la costante che specifica la dimensione o l'indice della matrice.

La matrice deve essere associata all'identificatore specificato dall'attributo field nel modo seguente: quando la matrice è un parametro, l'identificatore deve essere anche un parametro per la stessa funzione. Quando la matrice è un campo della struttura, l'identificatore deve essere un altro campo struttura della stessa struttura.

Una matrice viene chiamata "conforme" Se il limite superiore di una dimensione viene determinato in fase di esecuzione. Solo i limiti superiori possono essere determinati in fase di esecuzione. Per determinare il limite superiore, la dichiarazione di matrice deve includere [**una \_ dimensione**](size-is.md) oppure il valore [**massimo \_ è**](max-is.md) attributo.

Una matrice viene chiamata "varying" quando i relativi limiti vengono determinati in fase di compilazione, ma l'intervallo di elementi trasmessi viene determinato in fase di esecuzione. Per determinare l'intervallo di elementi trasmessi, la dichiarazione di matrice deve includere [**una \_ lunghezza**](length-is.md), ovvero il [**primo \_ è**](first-is.md)o [**l'ultimo \_**](last-is.md) attributo.

Una matrice di variabili conformi (detta anche "Open") è una matrice il cui limite superiore e l'intervallo di elementi trasmessi vengono determinati in fase di esecuzione. Al massimo, una matrice di variabili conforme o conforme può essere annidata in una struttura C e deve essere l'ultimo elemento della struttura. Al contrario, le matrici variabili non conformi possono essere presenti in qualsiasi punto di una struttura.

## <a name="examples"></a>Esempio

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

Per altre informazioni, vedere [matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Matrici multidimensionali

L'utente può dichiarare tipi che sono matrici e quindi dichiarare matrici di oggetti di tali tipi. La semantica delle matrici *m*-dimensionali dei tipi di matrici a *n* dimensioni corrisponde alla semantica delle  + matrici *n*-dimensionali m.

Il tipo RECT, ad esempio, \_ può essere definito come matrice bidimensionale e la variabile *Rect* può essere definita come una matrice di \_ tipo Rect. Equivale alla matrice tridimensionale *equivalente a \_ Rect*:

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Microsoft RPC è orientato a C. Secondo le convenzioni del linguaggio C, solo la prima dimensione di una matrice multidimensionale può essere determinata in fase di esecuzione. L'interazione con le matrici IDL DCE che supportano altri linguaggi è limitata a:

-   Matrici multidimensionali con limiti costanti (in fase di compilazione).
-   Matrici multidimensionali con tutti i limiti costanti eccetto la prima dimensione. Il limite superiore e l'intervallo di elementi trasmessi della prima dimensione dipendono dal runtime.
-   Qualsiasi matrice unidimensionale con limite inferiore pari a zero.

Quando l' **\[** [](string.md) **\]** attributo stringa viene utilizzato nelle matrici multidimensionali, l'attributo si applica alla matrice più a destra.

## <a name="arrays-of-pointers"></a>Matrici di puntatori

I puntatori di riferimento devono puntare a dati validi. L'applicazione client deve allocare tutta la memoria per un oggetto o in una **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** matrice di puntatori di riferimento, soprattutto quando la matrice è associata a **\[ in \]**, o **\[** **in \] , out**, **\[** [**length \_ is**](length-is.md) **\]** o **\[** [**Last \_ è**](last-is.md) **\]** values. L'applicazione client deve anche inizializzare tutti gli elementi della matrice prima della chiamata. Prima di tornare al client, l'applicazione server deve verificare che tutti gli elementi della matrice nell'intervallo trasmesso puntino a un archivio valido.

Sul lato server, lo stub alloca spazio di archiviazione per tutti gli elementi della matrice, indipendentemente dalla **\[** [**lunghezza \_**](length-is.md) **\]** o dall' **\[** [**ultimo \_**](last-is.md) **\]** valore al momento della chiamata. Questa funzionalità può influire sulle prestazioni dell'applicazione.

Nessuna restrizione viene posizionata sulle matrici di puntatori univoci. Nel client e nel server, lo spazio di archiviazione viene allocato per i puntatori null. Quando i puntatori sono non null, i dati vengono inseriti in un'archiviazione preallocata.

Un dichiaratore di puntatore facoltativo può precedere il dichiaratore di matrice.

Quando i puntatori di riferimento incorporati sono **\[** [](out-idl.md) **\]** parametri di sola uscita, il codice server-Manager deve assegnare valori validi alla matrice di puntatori di riferimento. Ad esempio:

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

Gli stub generati allocano la matrice e assegnano valori null a tutti i puntatori incorporati nella matrice.

 

 