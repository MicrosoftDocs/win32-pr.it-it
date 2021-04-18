---
title: LISTBOX. fontFace
description: L'attributo fontFace specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- Media Player di Windows LISTBOX. fontFace
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327749"
---
# <a name="listboxfontface"></a>LISTBOX. fontFace

L'attributo **fontFace** specifica o Recupera il tipo di carattere per il controllo casella di riepilogo.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows. Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.

Se il **fontFace** specificato non è disponibile nel sistema dell'utente, l'impostazione predefinita del controllo casella di riepilogo è il tipo di carattere di sistema Windows. Il valore predefinito per i sistemi in lingua inglese è "Tahoma". Per i sistemi internazionali, il valore predefinito viene caricato da un file di risorse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> <dt>

[**LISTBOX. fontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





