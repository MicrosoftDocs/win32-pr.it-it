---
title: Numeri interi grandi
description: Le funzioni e le strutture Integer di grandi dimensioni forniscono originariamente supporto per i valori a 64 bit nelle finestre a 32 bit.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- numeri interi grandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300262"
---
# <a name="large-integers"></a>Numeri interi grandi

Le funzioni e le strutture Integer di grandi dimensioni forniscono originariamente supporto per i valori a 64 bit nelle finestre a 32 bit. A questo punto, il compilatore C può supportare interi a 64 bit a livello nativo. Ad esempio, Microsoft Visual C++ supporta il tipo Integer di dimensioni [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Per ulteriori informazioni, vedere la documentazione inclusa con il compilatore C.

Per informazioni sugli Integer a 64 bit in Windows a 64 bit, vedere [i nuovi tipi di dati](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Operazioni integer di grandi dimensioni

Le applicazioni possono moltiplicare interi a 32 bit firmati o senza segno, generando risultati a 64 bit, usando le funzioni [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) e [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) . Le applicazioni possono spostare i bit nei valori a 64 bit a sinistra o a destra usando le funzioni [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)e [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) . Queste funzioni forniscono lo spostamento logico e aritmetico.

Le applicazioni possono anche moltiplicare e dividere i valori a 32 bit in un'unica operazione usando la funzione [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) . Sebbene il risultato dell'operazione sia un valore a 32 bit, la funzione archivia il risultato intermedio come valore a 64 bit, in modo che le informazioni non vadano perse quando si moltiplicano e si suddividono valori di grandi dimensioni a 32 bit.

## <a name="large-integer-reference"></a>Riferimento Integer grande

-   [Funzioni Integer di grandi dimensioni](large-integer-functions.md)
-   [Strutture Integer grandi](large-integer-structures.md)

 

 