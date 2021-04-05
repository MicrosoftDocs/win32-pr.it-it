---
title: Applicazione autonoma
description: Questa applicazione autonoma, che è costituita da una chiamata a una singola funzione, costituisce la base dell'applicazione distribuita.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044710"
---
# <a name="the-standalone-application"></a>Applicazione autonoma

Questa applicazione autonoma, che è costituita da una chiamata a una singola funzione, costituisce la base dell'applicazione distribuita. La funzione **HelloProc** è definita nel proprio file di origine, in modo che possa essere compilata e collegata con un'applicazione autonoma o un'applicazione distribuita.


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 




