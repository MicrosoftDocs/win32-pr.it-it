---
title: Convenzioni di stile di codifica
description: In questa serie di esempio vengono usate convenzioni di stile di codifica per facilitare la chiarezza e la coerenza.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd6f45fcff7e8f5f8e6f152ec1449bdf12170028537fd4b579d25479572dc5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962441"
---
# <a name="coding-style-conventions"></a>Convenzioni di stile di codifica

In questa serie di esempio vengono usate convenzioni di stile di codifica per facilitare la chiarezza e la coerenza. Vengono usate le convenzioni di notazione "ungheresi". Queste sono diventate una pratica di codifica comune nella programmazione Win32. Includono notazioni di prefisso di variabile che forniscono ai nomi delle variabili un suggerimento del tipo della variabile.

Nella tabella seguente sono elencati i prefissi comuni.



| Prefisso | Descrizione                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| Cb     | Conteggio dei byte                      |
| Cr     | Valore di riferimento del colore               |
| Cx     | Conteggio di x (short)                  |
| dw     | DWORD (unsigned long)               |
| f      | Flag (in genere più valori di bit) |
| fn     | Funzione                            |
| G\_    | Globale                              |
| h      | Handle                              |
| i      | Intero                             |
| l      | long                                |
| lp     | Puntatore long                        |
| m\_    | Membro dati di una classe              |
| n      | Short int                           |
| p      | Puntatore                             |
| s      | string                              |
| sz     | Stringa con terminazione zero              |
| tm     | Metrica del testo                         |
| u      | Unsigned int                        |
| ul     | Unsigned long (ULONG)               |
| w      | WORD (unsigned short)               |
| x,y    | Coordinate x, y (short)            |



 

Questi vengono spesso combinati, come nell'esempio seguente.



| Combinazione di prefissi | Descrizione                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Puntatore a una stringa.                                  |
| m \_ pszMyString     | Puntatore a una stringa che è un membro dati di una classe. |



 

Nella tabella seguente sono elencate altre convenzioni.



| Convenzione       | Descrizione                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Prefisso 'C' per i nomi di classe C++.                          |
| COMyObjectClass  | Prefisso 'CO' per i nomi delle classi di oggetti COM.                  |
| CFMyClassFactory | Prefisso 'CF' per i nomi class factory COM.                 |
| Interfaccia IMyInterface     | Prefisso 'I' per i nomi delle classi di interfaccia COM.                |
| CImpIMyInterface | Prefisso 'CImpI' per le classi di implementazione dell'interfaccia COM. |



 

In questa serie di esempio vengono usate alcune convenzioni coerenti per i blocchi di intestazione dei commenti, come indicato di seguito.

## <a name="file-header"></a>Intestazione file

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Blocco di commenti normale

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Intestazione dichiarazione di classe

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>Intestazione di definizione del metodo di classe

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Funzione non esportata o locale

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>Intestazione della definizione di funzione esportata

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>Intestazione della dichiarazione di interfaccia COM

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>Intestazione della dichiarazione della classe di oggetti COM

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Tutte queste convenzioni di blocco di commento hanno stringhe di token di inizio e di fine coerenti. Questa coerenza supporta in qualche modo l'elaborazione automatica delle intestazioni. Ad esempio, gli script AWK possono essere scritti per filtrare le intestazioni di funzione in un file di testo separato che può quindi fungere da base per un documento di specifica. Analogamente, è possibile usare strumenti come l'utilità AUTODUCK non supportata (attualmente disponibile nel CD-ROM della libreria di sviluppo di rete di Sviluppatore Microsoft) per elaborare i blocchi di commento in queste intestazioni.

Nella tabella seguente sono elencate le stringhe di token di inizio e di fine usate nelle esercitazioni di esempio.



| token | Descrizione                      |
|-------|----------------------------------|
| /\*+  | Inizio intestazione file                |
| +\*/  | Fine intestazione file                  |
| /\*-  | Inizio intestazione blocco di commento normale |
| -\*/  | Fine intestazione del blocco di commenti normale   |
| /\*C  | Inizio intestazione classe               |
| C\*/  | Fine intestazione classe                 |
| /\*M  | Inizio intestazione metodo              |
| M\*/  | Fine intestazione metodo                |
| /\*F  | Inizio intestazione funzione            |
| F\*/  | Fine intestazione funzione              |
| /\*Ho  | Inizio intestazione interfaccia           |
| Ho\*/  | Fine intestazione interfaccia             |
| /\*O  | Inizio intestazione classe oggetto COM    |
| O\*/  | Fine intestazione classe oggetto COM      |



 

Queste intestazioni possono essere usate anche come segnali visivi per l'analisi rapida dei file di origine. Offrono anche praticità per raggiungere rapidamente una posizione di origine se si configurano stringhe di ricerca nell'editor e quindi si "ripete l'ultima ricerca" per individuare rapidamente queste intestazioni.

Ad esempio, la stringa di ricerca "M+M" individua l'inizio delle intestazioni del metodo e "M-M" individua l'inizio del codice di definizione/implementazione effettivo del metodo.

 

 




