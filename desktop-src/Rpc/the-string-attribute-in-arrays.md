---
title: Attributo string nelle matrici
description: È possibile usare l'attributo \ string\ per matrici di caratteri unidimensionali, matrici di caratteri wide e matrici di byte che rappresentano stringhe di testo.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d56099c9cc2be3638642b20f6d3572786ea0a93f47f8660c2e847c4c06dd3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016661"
---
# <a name="the-string-attribute-in-arrays"></a>Attributo \[ \] string nelle matrici

È possibile usare \[ [l'attributo stringa](/windows/desktop/Midl/string) per matrici di caratteri unidimensionali, matrici di caratteri wide e \] matrici di byte che rappresentano stringhe di testo. Se si usa l'attributo **\[ string, \]** lo stub client usa le funzioni della libreria C **strlen** o **wstrlen** per contare il numero di caratteri nella stringa. Per evitare possibili incoerenze, MIDL **\[ \]** non consente di usare l'attributo stringa nello stesso momento in cui il primo è , \[ [ \_](/windows/desktop/Midl/first-is)last \] \[ [ \_ è](/windows/desktop/Midl/last-is)e size \] \[ [ \_ è](/windows/desktop/Midl/size-is) \] attributes.

Con le stringhe con terminazione Null in C, è necessario consentire lo spazio per il carattere Null alla fine della stringa. Ad esempio, quando si dichiara una stringa che contiene fino a 80 caratteri, allocare 81 caratteri. Il file IDL di esempio seguente illustra come dichiarare matrici con **\[ l'attributo string. \]**

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 