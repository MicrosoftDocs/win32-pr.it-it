---
title: CASELLA. fontFace
description: L'attributo fontFace specifica o Recupera il tipo di carattere per il testo nel controllo casella di modifica.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Media Player Windows casella. fontFace
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331589"
---
# <a name="editboxfontface"></a>CASELLA. fontFace

L'attributo **fontFace** specifica o Recupera il tipo di carattere per il testo nel controllo casella di modifica.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows. Windows Media Player non supporterà l'installazione dei tipi di carattere. Pertanto, scegliere un tipo di carattere che sarà noto nel sistema previsto.

Se il **fontFace** specificato non è disponibile nel sistema dell'utente, il controllo casella di modifica viene impostato sul tipo di carattere di sistema Windows. Il valore predefinito per i sistemi in lingua inglese è "Tahoma". Per i sistemi internazionali, il valore predefinito viene caricato da un file di risorse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento casella**](editbox-element.md)
</dt> <dt>

[**CASELLA. fontSize**](editbox-fontsize.md)
</dt> <dt>

[**CASELLA. fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





