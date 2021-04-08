---
title: Importazione di file di intestazione di sistema
description: Sebbene sia spesso possibile utilizzare la direttiva \ include per includere i file di intestazione nel file IDL, non è consigliabile.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importazione di MIDL, file di intestazione di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761590"
---
# <a name="importing-system-header-files"></a>Importazione di file di intestazione di sistema

Sebbene sia spesso possibile utilizzare la direttiva **\# include** per includere i file di intestazione nel file IDL, non è consigliabile. Il compilatore MIDL genererà gli stub per tutte le funzioni definite nel file IDL da compilare. In genere, un file di intestazione contiene un numero di prototipi che non è necessario né includere nei file stub e un' **\# inclusione** inserisce efficacemente tutte le definizioni nel file IDL principale. Inoltre, se nel file di intestazione sono definiti tipi non, il file IDL potrebbe non essere compilato.

Esistono due modi per includere le definizioni dei tipi dai file di intestazione in un file IDL:

-   Utilizzare la direttiva [**Import**](import.md) per includere i tipi di dati definiti in un file di intestazione. A differenza della direttiva di **\# inclusione** del linguaggio C, la direttiva **Import** preleva solo le definizioni di tipo e costante e ignora i prototipi di procedura. Questo approccio funzionerà purché il file IDL principale non faccia riferimento ad alcun tipo non definito nel file di intestazione.
-   Creare un file IDL helper con un'interfaccia fittizia che includa i file di intestazione. Usare quindi la direttiva [**Import**](import.md) per includere il file helper. In questo modo, solo i [**typedef**](typedef.md)verranno visualizzati negli Stub compilati. Ad esempio:

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
