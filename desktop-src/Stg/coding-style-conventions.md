---
title: Convenzioni di stile di codifica
description: Le convenzioni di stile del codice vengono usate in questa serie di esempi per facilitare la chiarezza e la coerenza.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734962"
---
# <a name="coding-style-conventions"></a>Convenzioni di stile di codifica

Le convenzioni di stile del codice vengono usate in questa serie di esempi per facilitare la chiarezza e la coerenza. Vengono utilizzate le convenzioni di notazione "ungherese". Questi sono diventati una procedura di codifica comune nella programmazione Win32. Includono la notazione del prefisso variabile che assegna ai nomi delle variabili un suggerimento del tipo della variabile.

Nella tabella seguente sono elencati i prefissi comuni.



| Prefisso | Descrizione                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| CB     | Conteggio di byte                      |
| CR     | Valore riferimento colore               |
| CX     | Conteggio di x (Short)                  |
| dw     | DWORD (unsigned long)               |
| f      | Flag (in genere più valori di bit) |
| fn     | Funzione                            |
| g\_    | Globale                              |
| h      | Handle                              |
| i      | Integer                             |
| l      | long                                |
| lp     | Puntatore lungo                        |
| m\_    | Membro dati di una classe              |
| n      | Int breve                           |
| p      | Puntatore                             |
| s      | string                              |
| sz     | Stringa con terminazione zero              |
| tm     | Metrica testo                         |
| u      | Int senza segno                        |
| ul     | Long senza segno (ULONG)               |
| w      | WORD (unsigned short)               |
| x, y    | coordinate x, y (Short)            |



 

Questi vengono spesso combinati, come nell'esempio seguente.



| Combinazione di prefisso | Descrizione                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Puntatore a una stringa.                                  |
| \_pszMyString m     | Puntatore a una stringa che rappresenta un membro dati di una classe. |



 

Le altre convenzioni sono elencate nella tabella seguente.



| Convenzione       | Descrizione                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Prefisso "C" per i nomi delle classi C++.                          |
| COMyObjectClass  | Prefisso "CO" per i nomi delle classi di oggetti COM.                  |
| CFMyClassFactory | Prefisso "CF" per i nomi di class factory COM.                 |
| IMyInterface     | Prefisso "I" per i nomi delle classi di interfacce COM.                |
| CImpIMyInterface | Prefisso ' CImpI ' per le classi di implementazione dell'interfaccia COM. |



 

Alcune convenzioni coerenti per i blocchi di intestazione dei commenti vengono usate in questa serie di esempio come indicato di seguito.

## <a name="file-header"></a>Intestazione del file

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

## <a name="plain-comment-block"></a>Blocco di commento semplice

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Intestazione della dichiarazione di classe

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

## <a name="class-method-definition-header"></a>Intestazione definizione metodo classe

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

## <a name="unexported-or-local-function"></a>Funzione locale o non esportata

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

## <a name="exported-function-definition-header"></a>Intestazione di definizione della funzione esportata

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

## <a name="com-interface-declaration-header"></a>Intestazione di dichiarazione dell'interfaccia COM

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

## <a name="com-object-class-declaration-header"></a>Intestazione di dichiarazione della classe di oggetti COM

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

Tutte le convenzioni di blocco di commento hanno stringhe di token iniziali e finali coerenti. Questa coerenza supporta l'elaborazione automatica delle intestazioni in qualche modo. È ad esempio possibile scrivere script AWK per filtrare le intestazioni di funzione in un file di testo separato che può quindi fungere da base per un documento di specifica. Analogamente, è possibile usare strumenti come l'utilità di autoduck non supportata (attualmente disponibile nel CD-ROM della libreria di sviluppo della rete per sviluppatori Microsoft) per elaborare i blocchi di commento in queste intestazioni.

Nella tabella seguente sono elencate le stringhe dei token iniziali e finali utilizzate nelle esercitazioni di esempio.



| token | Descrizione                      |
|-------|----------------------------------|
| /\*+  | Inizio intestazione file                |
| +\*/  | Fine intestazione file                  |
| /\*-  | Inizio intestazione blocco commento normale |
| -\*/  | Fine intestazione blocco commento semplice   |
| /\*C  | Inizio intestazione classe               |
| C\*/  | Fine intestazione classe                 |
| /\*M  | Inizio intestazione metodo              |
| M\*/  | Fine intestazione metodo                |
| /\*F  | Inizio intestazione funzione            |
| F\*/  | Fine intestazione funzione              |
| /\*I  | Inizio intestazione interfaccia           |
| I\*/  | Fine intestazione interfaccia             |
| /\*O  | Inizio intestazione classe oggetto COM    |
| O\*/  | Fine intestazione classe oggetto COM      |



 

Queste intestazioni possono essere utilizzate anche come segnali visivi per l'analisi rapida dei file di origine. Consentono inoltre di accedere rapidamente ad alcune posizioni di origine se si configurano stringhe di ricerca nell'editor e quindi si ripete l'ultima ricerca per individuare rapidamente tali intestazioni.

Ad esempio, la stringa di ricerca "M + M" individua l'inizio delle intestazioni del metodo e "M-M" individua l'inizio del codice effettivo di definizione/implementazione del metodo.

 

 




