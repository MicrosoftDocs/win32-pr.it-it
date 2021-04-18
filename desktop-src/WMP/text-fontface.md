---
title: TESTO. fontFace
description: L'attributo fontFace specifica o Recupera il carattere tipografico per il controllo di testo.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Media Player di Windows TEXT. fontFace
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329426"
---
# <a name="textfontface"></a>TESTO. fontFace

L'attributo **fontFace** specifica o Recupera il carattere tipografico per il controllo di testo.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows. Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.

Se il **fontFace** specificato non è disponibile nel sistema dell'utente, per impostazione predefinita il controllo testo è il tipo di carattere di sistema Windows.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. fontSize**](text-fontsize.md)
</dt> </dl>

 

 





