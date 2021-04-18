---
title: Convenzioni di codifica Windows
description: Se non si ha familiarità con la programmazione Windows, può essere sconcertante quando viene visualizzato per la prima volta un programma Windows.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299642"
---
# <a name="windows-coding-conventions"></a>Convenzioni di codifica Windows

Se non si ha familiarità con la programmazione Windows, può essere sconcertante quando viene visualizzato per la prima volta un programma Windows. Il codice viene compilato con definizioni di tipo strano, ad esempio **DWORD \_ ptr** e **lpRect**, e le variabili hanno nomi quali *HWND* e *PWSZ* (denominata notazione ungherese). È opportuno apprendere alcune delle convenzioni di codifica di Windows.

La maggior parte delle API di Windows è costituita da funzioni o interfacce di Component Object Model (COM). Poche API Windows sono fornite come classi C++. Un'eccezione significativa è GDI+, una delle API grafiche 2D.

## <a name="typedefs"></a>Typedef

Le intestazioni di Windows contengono numerosi typedef. Molti di questi vengono definiti nel file di intestazione WinDef. h. Di seguito sono riportati alcuni dei problemi che si verificheranno spesso.

### <a name="integer-types"></a>Tipi integer



| Tipo di dati     | Dimensione    | Con segno?  |
|---------------|---------|----------|
| **BYTE**      | 8 bit  | Senza segno |
| **DWORD**     | 32 bit | Senza segno |
| **INT32**     | 32 bit | Firmato   |
| **INT64**     | 64 bit | Firmato   |
| **LONG**      | 32 bit | Firmato   |
| **LONGLONG**  | 64 bit | Firmato   |
| **UINT32**    | 32 bit | Senza segno |
| **UINT64**    | 64 bit | Senza segno |
| **ULONG**     | 32 bit | Senza segno |
| **ULONGLONG** | 64 bit | Senza segno |
| **WORD**      | 16 bit | Senza segno |



 

Come si può notare, in questi typedef esiste una certa quantità di ridondanza. Alcune di queste sovrapposizioni sono semplicemente dovute alla cronologia delle API di Windows. I tipi elencati di seguito hanno dimensioni fisse e le dimensioni sono le stesse nelle applicazioni a 32 bit e 64. Il tipo **DWORD** , ad esempio, è sempre di 32 bit.

### <a name="boolean-type"></a>Tipo Boolean

**Bool** è un typedef per un valore integer usato in un contesto booleano. Il file di intestazione WinDef. h definisce anche due valori da usare con **bool**.


```C++
#define FALSE    0 
#define TRUE     1
```



Nonostante questa definizione di **true**, tuttavia, la maggior parte delle funzioni che restituiscono un tipo **bool** può restituire qualsiasi valore diverso da zero per indicare la verità booleana. Pertanto, è sempre necessario scrivere questo:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



e non:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Tenere presente che **bool** è un tipo integer e non è interscambiabile con il tipo C++ **bool** .

### <a name="pointer-types"></a>Tipi di puntatore

Windows definisce molti tipi di dati del form *puntatore a X*. In genere il prefisso *P-* o *LP-* nel nome. Ad esempio, **lpRect** è un puntatore a un oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)), dove **Rect** è una struttura che descrive un rettangolo. Le seguenti dichiarazioni di variabili sono equivalenti.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



In passato, *P* sta per "pointer" e *LP* sta per "Long pointer". I puntatori lunghi (detti anche *puntatori lontani*) sono retaggio da Windows a 16 bit, quando sono necessari per indirizzare gli intervalli di memoria all'esterno del segmento corrente. Il prefisso *LP* è stato mantenuto per semplificare la porta del codice a 16 bit in Windows a 32 bit. Attualmente non esiste alcuna distinzione: un puntatore è un puntatore.

### <a name="pointer-precision-types"></a>Tipi di precisione del puntatore

I tipi di dati riportati di seguito sono sempre le dimensioni di un puntatore, ovvero 32 bit a larghezza nelle applicazioni a 32 bit e 64 bit in larghezza nelle applicazioni a 64 bit. La dimensione viene determinata in fase di compilazione. Quando un'applicazione a 32 bit viene eseguita in Windows a 64 bit, questi tipi di dati sono ancora di 4 byte. Non è possibile eseguire un'applicazione a 64 bit su Windows a 32 bit, quindi non si verifica la situazione inversa.

-   **\_ptr DWORD**
-   **\_ptr int**
-   **LONG \_ ptr**
-   **\_ptr ULONG**
-   **\_ptr uint**

Questi tipi vengono utilizzati nelle situazioni in cui è possibile eseguire il cast di un numero intero a un puntatore. Vengono inoltre utilizzate per definire le variabili per l'aritmetica dei puntatori e per definire i contatori del ciclo che eseguono l'iterazione sull'intervallo completo di byte nei buffer di memoria. Più in generale, vengono visualizzati in posizioni in cui un valore esistente a 32 bit è stato espanso a 64 bit in Windows a 64 bit.

## <a name="hungarian-notation"></a>Notazione ungherese

La *notazione ungherese* è la pratica di aggiungere i prefissi ai nomi delle variabili, per fornire informazioni aggiuntive sulla variabile. (L'inventore della notazione, Charles Simonyi, era ungherese, quindi il suo nome).

Nella sua forma originale, la notazione ungherese fornisce informazioni *semantiche* su una variabile, che indicano l'uso previsto. Ad esempio, un indice, *CB* indica una dimensione in byte ("count of bytes") e *i* numeri di riga e di colonna di *RW* e *col* mean. Questi prefissi sono progettati per evitare l'uso accidentale di una variabile nel contesto errato. Se, ad esempio, l'espressione è stata riguardata `rwPosition +  cbTable` , è possibile che venga aggiunto un numero di riga a una dimensione, che è quasi certamente un bug nel codice

Una forma più comune di notazione ungherese usa i prefissi per fornire informazioni sul *tipo* , ad esempio *DW* per **DWORD** e *w* per **Word**.

Se si esegue una ricerca nel Web di "notazione ungherese", sono disponibili numerose opinioni sulla presenza di una notazione ungherese valida o negativa. Alcuni programmatori hanno un'intensa antipatia per la notazione ungherese. Altri lo trovano utile. Indipendentemente, molti degli esempi di codice su MSDN usano la notazione ungherese, ma non è necessario memorizzare i prefissi per comprendere il codice.

## <a name="next"></a>Prossima

[Uso delle stringhe](working-with-strings.md)

 

 