---
title: Importazione di file di intestazione di sistema
description: Sebbene sia spesso possibile usare la direttiva \ include per includere i file di intestazione nel file IDL, non è consigliabile.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importazione di MIDL, file di intestazione di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070351ecd47b24d16d3baa2dde33b0199b02f4bf12e8ccc8f5628564a88dd6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383878"
---
# <a name="importing-system-header-files"></a>Importazione di file di intestazione di sistema

Sebbene sia spesso possibile usare la direttiva **\# include** per includere i file di intestazione nel file IDL, non è consigliabile. Il compilatore MIDL genererà stub per tutte le funzioni definite nel file IDL da compilare. In genere un file di intestazione contiene un numero di prototipi che non **\#** è necessario né si vuole includere nei file stub e un'inclusione inserisce in modo efficace tutte le definizioni nel file IDL principale. Inoltre, se nel file di intestazione sono definiti tipi nonremobili, il file IDL potrebbe non essere compilato.

Esistono due modi per includere le definizioni dei tipi dai file di intestazione in un file IDL:

-   Usare la [**direttiva import**](import.md) per includere i tipi di dati definiti in un file di intestazione. A differenza della direttiva **\# include del linguaggio** C, la direttiva **import** preleva solo le definizioni di tipi e costanti e ignora i prototipi di routine. Questo approccio funzionerà purché il file IDL principale non fa riferimento a tipi nonremobili definiti nel file di intestazione.
-   Creare un file IDL helper con un'interfaccia fittizia che include i file di intestazione. Usare quindi la direttiva [**import**](import.md) per includere il file helper. In questo modo, solo [**i typedef**](typedef.md)verranno visualizzati negli stub compilati. Ad esempio:

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
