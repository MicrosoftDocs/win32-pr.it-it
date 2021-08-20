---
title: Tabelle di funzioni virtuali
description: Tabelle di funzioni virtuali
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135498"
---
# <a name="virtual-function-tables"></a>Tabelle di funzioni virtuali

Una tabella di funzioni virtuali è una matrice di puntatori ai metodi supportati da un oggetto. Se si usa C, un oggetto viene visualizzato come una struttura il cui primo membro è un puntatore alla tabella della funzione virtuale (**lpVtbl**); il primo membro punta a una matrice contenente puntatori a funzione. Tutti i metodi accettano un puntatore alla tabella di funzioni come primo parametro. Nell'esempio seguente viene quindi chiamato il **metodo Read** di un **oggetto pStream:**


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



In C+ + il puntatore alla tabella della funzione virtuale, *il puntatore this,* è implicito. L'esempio seguente equivale all'esempio precedente quando si usa C+ +:


```C++
pStream->Read(parameters) 
 
```



 

 




