---
title: TEXT.fontFace
description: L'attributo fontFace specifica o recupera il carattere tipografico per il controllo Text.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Text.fontFace Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b1044d01ac3ca6a8cc4f1212232bfcc630eb73831f90eb7fd5f423f5dc38d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118358"
---
# <a name="textfontface"></a>TEXT.fontFace

**L'attributo fontFace** specifica o recupera il carattere tipografico per il controllo Text.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile Windows. Windows Media Player non supporterà l'installazione dei tipi di carattere, quindi scegliere un tipo di carattere che si sa sarà nel sistema previsto.

Se il **carattere fontFace** specificato non è disponibile nel sistema dell'utente, il controllo Text viene utilizzato per impostazione predefinita Windows di sistema.

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontSize**](text-fontsize.md)
</dt> </dl>

 

 





