---
title: Tabelle di funzioni virtuali
description: Tabelle di funzioni virtuali
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297890"
---
# <a name="virtual-function-tables"></a>Tabelle di funzioni virtuali

Una tabella di funzioni virtuali è una matrice di puntatori ai metodi supportati da un oggetto. Se si usa C, un oggetto viene visualizzato come una struttura il cui primo membro è un puntatore alla tabella della funzione virtuale (**lpVtbl**); ovvero, il primo membro punta a una matrice che contiene i puntatori a funzione. Tutti i metodi accettano un puntatore alla tabella di funzioni come primo parametro. Nell'esempio seguente viene quindi chiamato il metodo **Read** di un oggetto **pStream** :


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



In C + + il puntatore alla tabella della funzione virtuale, il puntatore *this* , è implicito. Il codice seguente è equivalente all'esempio precedente quando si usa C + +:


```C++
pStream->Read(parameters) 
 
```



 

 




