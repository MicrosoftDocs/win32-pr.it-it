---
title: Suggerimenti sulla migrazione
description: È importante prendere in considerazione i calcoli degli indirizzi e l'aritmetica dei puntatori quando si esegue la portabilità del codice in un Windows a 64 bit.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guida alla programmazione a 64 bit Windows programmazione a 64 bit Windows programmazione a 64 bit, suggerimenti per la migrazione
- suggerimenti per la migrazione programmazione Windows a 64 bit
- Compatibilità a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743596"
---
# <a name="migration-tips"></a>Suggerimenti sulla migrazione

Le due principali aree di interesse quando si esamina il codice per la compatibilità a 64 bit sono le seguenti:

-   Calcoli degli indirizzi
-   Puntatore aritmetico

Per molti motivi, gli sviluppatori hanno archiviato gli indirizzi come **valore ULONG.** Dopo tutto, in un Windows a 32 bit, un indirizzo, un puntatore e un valore **ULONG** sono tutti a 32 bit. Tuttavia, in caso di Windows a 64 bit, un indirizzo e un **ULONG** non hanno la stessa lunghezza. Mentre un **ULONG** rimane un valore a 32 bit, tutti i puntatori sono ora valori a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Linee guida generali sulla portabilità](general-porting-guidelines.md)
-   [Archiviazione di un valore a 64 bit](storing-a-64-bit-value.md)
-   [Errori comuni del compilatore](common-compiler-errors.md)
-   [Considerazioni aggiuntive](additional-considerations.md)

 

 




