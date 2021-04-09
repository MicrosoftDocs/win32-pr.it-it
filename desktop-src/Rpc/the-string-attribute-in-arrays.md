---
title: Attributo stringa nelle matrici
description: È possibile usare l'attributo \ string \ per matrici di caratteri unidimensionali, matrici di caratteri wide e matrici di byte che rappresentano stringhe di testo.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118114"
---
# <a name="the-string-attribute-in-arrays"></a>\[Attributo stringa \] nelle matrici

È possibile utilizzare l' \[ [](/windows/desktop/Midl/string) \] attributo stringa per matrici di caratteri unidimensionali, matrici di caratteri wide e matrici di byte che rappresentano stringhe di testo. Se si usa l'attributo **\[ stringa \]** , lo stub client usa le funzioni della libreria C **strlen** o **wstrlen** per contare il numero di caratteri nella stringa. Per evitare possibili incoerenze, MIDL non consente di utilizzare l'attributo **\[ stringa \]** contemporaneamente al \[ [primo \_](/windows/desktop/Midl/first-is) \] , ovvero \[ [Last \_ is](/windows/desktop/Midl/last-is) \] e \[ [size \_ è](/windows/desktop/Midl/size-is) \] Attributes.

Con le stringhe con terminazione null in C, è necessario consentire lo spazio per il carattere null alla fine della stringa. Ad esempio, quando si dichiara una stringa che conterrà fino a 80 caratteri, allocare 81 caratteri. Nel file IDL di esempio seguente viene illustrato come dichiarare matrici con l'attributo di **\[ stringa \]** .

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

 

 