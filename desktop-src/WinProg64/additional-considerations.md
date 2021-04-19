---
title: Ulteriori considerazioni
description: Quando si porta il codice, considerare i punti seguenti.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Suggerimenti per il porting per la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323774"
---
# <a name="additional-considerations"></a>Ulteriori considerazioni

Quando si porta il codice, considerare i punti seguenti:

- Il presupposto seguente non è più valido:

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   Tuttavia, il compilatore a 64 bit definisce \_ Win32 per la compatibilità con le versioni precedenti.

- Il presupposto seguente non è più valido:

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   In questo caso, la clausola else può rappresentare \_ Win32 o \_ Win64.

- Prestare attenzione all'allineamento del tipo di dati. La macro di **\_ allineamento dei tipi** restituisce i requisiti di allineamento di un tipo di dati. Ad esempio: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 su x86, 8 su processore Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 ovunque

    Ad esempio, il codice del kernel che attualmente ha un aspetto simile al seguente:

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    è probabilmente necessario modificare in:

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

    Il problema è che ~ (b-1) produce "0x0000 0000 xxxx xxxx" e non "0xFFFF FFFF xxxx xxxx". Il compilatore non riuscirà a rilevare questo problema. Per risolvere il problema, modificare il codice nel modo seguente:

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- Prestare attenzione a eseguire operazioni senza segno e firmate. Considerare quanto segue:

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    Il risultato è inaspettatamente grande. La regola è che se uno degli operandi è senza segno, il risultato è senza segno. Nell'esempio precedente, un oggetto viene convertito in un valore senza segno, diviso per b, e il risultato archiviato in c. La conversione non prevede alcuna manipolazione numerica.

    Come altro esempio, tenere presente quanto segue:

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    Il problema si verifica perché x è senza segno, il che rende l'intera espressione senza segno. Questa operazione funziona correttamente, a meno che y non sia negativo. In questo caso, y viene convertito in un valore senza segno, l'espressione viene valutata con precisione a 32 bit, ridimensionata e aggiunta a pVar1. Un numero negativo senza segno a 32 bit diventa un numero positivo a 64 bit di grandi dimensioni, che fornisce il risultato errato. Per risolvere il problema, dichiarare x come valore con segno o typecast in modo esplicito a **Long** nell'espressione.

- Prestare attenzione quando si effettuano allocazioni di dimensioni a fasi. Ad esempio:

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    Il codice seguente non è corretto perché il compilatore riempie la struttura con altri 4 byte per rendere l'allineamento a 8 byte:

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    Il codice seguente è corretto:

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- Non passare `(HANDLE)0xFFFFFFFF` a funzioni come [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga). Usare invece un **\_ \_ valore di handle non valido**.
- Usare gli identificatori di formato corretti durante la stampa di una stringa. Utilizzare% p per stampare i puntatori in formato esadecimale. Questa è la scelta migliore per i puntatori alla stampa. Microsoft Visual C++ supporta% I per stampare i dati polimorfici. Visual C++ supporta anche% I64 per stampare valori con 64 bit.

 

 