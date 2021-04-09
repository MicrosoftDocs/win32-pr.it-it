---
title: Sezione bitmap
description: Sezione bitmap
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, bitmap
- interfacce, bitmap
- creazione di interfacce, sezione bitmap
- scrittura di codice per interfacce, sezione bitmap
- bitmap in interfacce, sezione bitmap
- file di definizione dell'interfaccia, sezione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044631"
---
# <a name="bitmaps-section"></a>Sezione bitmap

Successivamente, è necessario disporre di una sezione che definisce ognuno dei file bitmap. Ogni tipo di bitmap che verrà usato deve avere un file assegnato, sebbene sia possibile avere più di un tipo usando la stessa bitmap.


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



La sezione bitmap deve iniziare con le bitmap di Word tra parentesi quadre, quindi una riga per ogni tipo di bitmap che si vuole definire. In questo esempio sono stati definiti cinque tipi di bitmap. Per ulteriori informazioni sulla sezione bitmap, vedere [bitmap](bitmaps.md) nel riferimento all'interfaccia.

> [!Note]  
> L'area e le bitmap con privilegi avanzati sono deprecate in Windows Media Player 10 mobile o versioni successive.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura del codice**](writing-the-code.md)
</dt> </dl>

 

 




