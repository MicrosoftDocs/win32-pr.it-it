---
title: Ulteriori considerazioni
description: Quando si esegue la portabilità del codice, tenere presente quanto segue.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- porting tips 64-bit Windows Programming (Suggerimenti per la portabilità a 64 bit Windows programmazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 199f522bebf0d6d5552aa81d99aab12f77685dea35eb329b9e7d11d46b4f1500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561536"
---
# <a name="additional-considerations"></a>Ulteriori considerazioni

Quando si esegue la portabilità del codice, tenere presente quanto segue:

- Il presupposto seguente non è più valido:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Tuttavia, il compilatore a 64 bit definisce WIN32 per la \_ compatibilità con le versioni precedenti.

- Il presupposto seguente non è più valido:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   In questo caso, la clausola else può rappresentare \_ WIN32 o \_ WIN64.

- Prestare attenzione con l'allineamento del tipo di dati. La macro **TYPE \_ ALIGNMENT** restituisce i requisiti di allineamento di un tipo di dati. Ad esempio: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 su x86, 8 nel processore Intel Itanium `TYPE_ALIGNMENT( UCHAR )` == 1 ovunque

    Ad esempio, il codice del kernel è simile al seguente:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    probabilmente deve essere modificato in:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    Le correzioni automatiche delle eccezioni di allineamento in modalità kernel sono disabilitate per i sistemi Intel Itanium.

- Prestare attenzione con le operazioni NOT. Considerare quanto segue:

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    Il problema è che ~(b–1) produce "0x0000 0000 xxxx xxxx" e non "0xFFFF FFFF xxxx xxxx". Il compilatore non lo rileverà. Per risolvere il problema, modificare il codice come segue:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Prestare attenzione durante l'esecuzione di operazioni non firmate e firmate. Considerare quanto segue:

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    Il risultato è imprevistamente grande. La regola è che se uno degli operandi è senza segno, il risultato è senza segno. Nell'esempio precedente, a viene convertito in un valore senza segno, diviso per b, e il risultato viene archiviato in c. La conversione non comporta alcuna manipolazione numerica.

    Come altro esempio, si consideri quanto segue:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    Il problema si verifica perché x è senza segno, il che rende l'intera espressione senza segno. Questa operazione funziona correttamente a meno che y non sia negativo. In questo caso, y viene convertito in un valore senza segno, l'espressione viene valutata usando la precisione a 32 bit, ridimensionata e aggiunta a pVar1. Un numero negativo senza segno a 32 bit diventa un numero positivo a 64 bit elevato, che restituisce il risultato errato. Per risolvere questo problema, dichiarare x come valore con segno o eseguire in modo esplicito il cast del tipo a **LONG** nell'espressione.

- Prestare attenzione quando si effettuano allocazioni di dimensioni a frammenti. Esempio:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    Il codice seguente non è corretto perché il compilatore riempire la struttura con altri 4 byte per rendere l'allineamento a 8 byte:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    Il codice seguente è corretto:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Non passare a `(HANDLE)0xFFFFFFFF` funzioni come [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga). Usare invece **INVALID \_ HANDLE \_ VALUE**.
- Usare gli identificatori di formato corretto durante la stampa di una stringa. Usare %p per stampare i puntatori in formato esadecimale. Questa è la scelta migliore per la stampa dei puntatori. Microsoft Visual C++ supporta %I per stampare dati polimorfici. Visual C++ supporta anche %I64 per stampare valori a 64 bit.

 

 