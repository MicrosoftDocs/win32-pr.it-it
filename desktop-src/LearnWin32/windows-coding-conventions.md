---
title: Windows Convenzioni di codifica
description: Se non si ha esperienza Windows programmazione, può essere sconcertante quando viene visualizzato per la prima volta un Windows programma.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78c24f38f9f2f410c044637ca3aa59d4baa39e9b671b3485c5b85899b69c2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387396"
---
# <a name="windows-coding-conventions"></a>Windows Convenzioni di codifica

Se non si ha esperienza Windows programmazione, può essere sconcertante quando viene visualizzato per la prima volta un Windows programma. Il codice è pieno di definizioni di tipi sconosciute, ad esempio **DWORD \_ PTR** e **LPRECT,** e le variabili hanno nomi come *hWnd* *e pwsz* (chiamata notazione ungherese). Vale la pena prendere un po' di tempo per apprendere alcune delle Windows di scrittura del codice.

La maggior parte Windows API è costituita da funzioni o Component Object Model (COM). Pochissime Windows API vengono fornite come classi C++. Un'eccezione GDI+, una delle API grafiche 2D.

## <a name="typedefs"></a>Typedef

Le Windows contengono molti typedef. Molte di queste sono definite nel file di intestazione WinDef.h. Di seguito sono riportati alcuni esempi che si verificano spesso.

### <a name="integer-types"></a>Tipi integer



| Tipo di dati     | Dimensione    | Firmato?  |
|---------------|---------|----------|
| **BYTE**      | 8 bit  | Senza segno |
| **Dword**     | 32 bit | Senza segno |
| **INT32**     | 32 bit | Firmato   |
| **INT64**     | 64 bit | Firmato   |
| **LONG**      | 32 bit | Firmato   |
| **LONGLONG**  | 64 bit | Firmato   |
| **UINT32**    | 32 bit | Senza segno |
| **UINT64**    | 64 bit | Senza segno |
| **Ulong**     | 32 bit | Senza segno |
| **Ulonglong** | 64 bit | Senza segno |
| **WORD**      | 16 bit | Senza segno |



 

Come si può vedere, c'è una certa quantità di ridondanza in questi typedef. Alcune di queste sovrapposizioni sono semplicemente dovute alla cronologia delle API Windows. I tipi elencati hanno dimensioni fisse e le dimensioni sono le stesse nelle applicazioni a 32 bit e a 64 bit. Ad esempio, il **tipo DWORD** è sempre di 32 bit.

### <a name="boolean-type"></a>Tipo booleano

**BOOL** è un typedef per un valore integer usato in un contesto booleano. Il file di intestazione WinDef.h definisce anche due valori da usare con **BOOL**.


```C++
#define FALSE    0 
#define TRUE     1
```



Nonostante questa definizione di **TRUE,** tuttavia, la maggior parte delle funzioni che restituiscono un **tipo BOOL** può restituire qualsiasi valore diverso da zero per indicare la verità booleana. È pertanto consigliabile scrivere sempre questo codice:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



e non questo:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Tenere presente che **BOOL** è un tipo integer e non è intercambiabile con il tipo **bool** C++.

### <a name="pointer-types"></a>Tipi di puntatore

Windows definisce molti tipi di dati del formato *puntatore a X.* In genere hanno il prefisso *P-* *o LP-* nel nome. Ad esempio, **LPRECT** è un puntatore a [**rect**](/previous-versions//dd162897(v=vs.85)), dove **RECT** è una struttura che descrive un rettangolo. Le dichiarazioni di variabili seguenti sono equivalenti.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



P è  l'acronimo di "pointer" e *LP* è l'acronimo di "long pointer". I puntatori long (detti anche *puntatori* far) sono un blocco da Windows a 16 bit, quando erano necessari per risolvere gli intervalli di memoria al di fuori del segmento corrente. Il *prefisso LP* è stato mantenuto per semplificare la porta del codice a 16 bit a Windows. Attualmente non esiste alcuna distinzione: un puntatore è un puntatore.

### <a name="pointer-precision-types"></a>Tipi di precisione del puntatore

I tipi di dati seguenti sono sempre le dimensioni di un puntatore, ovvero 32 bit di larghezza nelle applicazioni a 32 bit e 64 bit di larghezza nelle applicazioni a 64 bit. Le dimensioni vengono determinate in fase di compilazione. Quando un'applicazione a 32 bit viene eseguita su Windows a 64 bit, questi tipi di dati sono ancora di 4 byte. Un'applicazione a 64 bit non può essere eseguita su Windows a 32 bit, quindi non si verifica la situazione inversa.

-   **DWORD \_ PTR**
-   **INT \_ PTR**
-   **LONG \_ PTR**
-   **ULONG \_ PTR**
-   **UINT \_ PTR**

Questi tipi vengono usati in situazioni in cui è possibile eseguire il cast di un integer a un puntatore. Vengono inoltre usate per definire variabili per l'aritmetica dei puntatori e per definire contatori del ciclo che esereranno l'intero intervallo di byte nei buffer di memoria. Più in generale, vengono visualizzati in posizioni in cui un valore a 32 bit esistente è stato espanso a 64 bit in Windows.

## <a name="hungarian-notation"></a>Notazione ungherese

*La notazione ungherese* è la pratica di aggiungere prefissi ai nomi delle variabili per fornire informazioni aggiuntive sulla variabile. (L'inventore della notazione, Charles Simonyi, era ungherese, da cui il nome).

Nella forma originale, la notazione ungherese fornisce informazioni *semantiche* su una variabile, indicando l'uso previsto. Ad esempio, *i* indica un indice, *cb* indica una dimensione in byte ("numero di byte") e i numeri di riga e colonna *rw* e *col* mean. Questi prefissi sono progettati per evitare l'uso accidentale di una variabile nel contesto errato. Ad esempio, se è stata vista l'espressione , si saprebbe che un numero di riga viene aggiunto a una dimensione, che è quasi certamente un `rwPosition +  cbTable` bug nel codice

Una forma più comune di notazione  ungherese usa i prefissi per fornire informazioni sul tipo, ad esempio *dw* per **DWORD** e *w* per **WORD**.

Se si cerca sul Web la "notazione ungherese", si noteranno molte opinioni sul fatto che la notazione ungherese sia buona o negativa. Alcuni programmatori hanno un'intensa antipatia per la notazione ungherese. Altri lo trovano utile. Indipendentemente da ciò, molti esempi di codice in MSDN usano la notazione ungherese, ma non è necessario memorizzare i prefissi per comprendere il codice.

## <a name="next"></a>Prossima

[Uso delle stringhe](working-with-strings.md)

 

 