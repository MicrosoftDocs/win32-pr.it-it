---
title: Registro indirizzi
description: Il registro a0 è un registro degli indirizzi.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856582"
---
# <a name="address-register"></a>Registro indirizzi

Il registro a0 è un registro degli indirizzi. Un singolo registro è disponibile nella versione di Visual Studio \_ 1 \_ . Il registro degli indirizzi, designato come a0. x in Visual Studio 1 \_ \_ , può essere usato come offset intero con segno per l'indirizzamento relativo nel file di registro delle costanti. Per le versioni vs \_ 2 \_ 0 e successive, tutti i quattro componenti (. x,. y,. z,. w) sono disponibili per l'indirizzamento relativo.


```
c[a0.x + n]
```



Il registro degli indirizzi non può essere letto da un vertex shader. può essere usato solo per l'indirizzamento relativo di un registro costante. La lettura di valori al di fuori dell'intervallo valido restituirà (0,0, 0,0, 0,0, 0,0). Il registro degli indirizzi può essere solo una destinazione per l'istruzione [MOV-vs](mov---vs.md) . Se un numero a virgola mobile viene spostato in un registro Integer, viene eseguita una conversione round-to-most più vicina.

Tutti gli shader devono inizializzare il registro degli indirizzi prima di usarlo. Per la versione vs \_ 2 \_ 0 e successive, l'istruzione [mova-vs](mova---vs.md) può spostare un valore a virgola mobile in un registro di indirizzi.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro indirizzi       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




