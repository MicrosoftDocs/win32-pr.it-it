---
title: Sezione Bitmaps
description: Sezione Bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, bitmap
- interfaccia, bitmap
- creazione di interfaccia, sezione Bitmap
- scrittura di codice per le interfaccia, sezione Bitmap
- bitmap nelle interfaccia, sezione Bitmap
- file di definizione dell'interfaccia utente, sezione Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3062a8679e916fc8eaa733ab82c3df51845969873fcf83534be5f9ec6e4c6f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573461"
---
# <a name="bitmaps-section"></a>Sezione Bitmaps

È quindi necessario disporre di una sezione che definisce ogni file bitmap. A ogni tipo di bitmap che verrà utilizzato deve essere assegnato un file, anche se è possibile avere più di un tipo usando la stessa bitmap.


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



La sezione Bitmaps deve iniziare con la parola Bitmaps tra parentesi quadre e quindi con una riga per ogni tipo di bitmap che si vuole definire. In questo esempio sono stati definiti cinque tipi di bitmap. Per altre informazioni sulla sezione Bitmap, vedere [Bitmap in](bitmaps.md) Riferimenti all'interfaccia.

> [!Note]  
> Le bitmap Region e Super sono deprecate in Windows Media Player 10 Mobile o versioni successive.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura del codice**](writing-the-code.md)
</dt> </dl>

 

 




