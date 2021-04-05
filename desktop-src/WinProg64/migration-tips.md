---
title: Suggerimenti sulla migrazione
description: È importante prendere in considerazione i calcoli degli indirizzi e l'aritmetica dei puntatori quando si porta il codice in Windows a 64 bit.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guida per programmatori Windows a 64 bit Guida alla programmazione Windows a 64 bit, suggerimenti per la migrazione
- Suggerimenti per la migrazione programmazione Windows a 64 bit
- compatibilità con la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711710"
---
# <a name="migration-tips"></a>Suggerimenti sulla migrazione

Le due principali aree di interesse quando si esamina il codice per la compatibilità a 64 bit sono le seguenti:

-   Calcoli degli indirizzi
-   Puntatore aritmetico

Per molti motivi, gli sviluppatori hanno archiviato gli indirizzi come valore **ULONG** . Dopo tutto, in Windows a 32 bit, un indirizzo, un puntatore e un valore **ULONG** sono tutti di 32 bit. Tuttavia, in Windows a 64 bit, un indirizzo e un **ULONG** non hanno la stessa lunghezza. Mentre un **ULONG** rimane un valore a 32 bit, tutti i puntatori sono ora valori a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Linee guida generali per il porting](general-porting-guidelines.md)
-   [Archiviazione di un valore a 64 bit](storing-a-64-bit-value.md)
-   [Errori comuni del compilatore](common-compiler-errors.md)
-   [Considerazioni aggiuntive](additional-considerations.md)

 

 




