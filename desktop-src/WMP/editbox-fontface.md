---
title: EDITBOX.fontFace
description: L'attributo fontFace specifica o recupera il tipo di carattere per il testo nel controllo casella di modifica.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EditBOX.fontFace Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3994c9cef1f645dc9c1129876b9144471caf9f608f5911641b180deae437194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996861"
---
# <a name="editboxfontface"></a>EDITBOX.fontFace

**L'attributo fontFace** specifica o recupera il tipo di carattere per il testo nel controllo casella di modifica.

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questo attributo può essere il nome di qualsiasi tipo di carattere valido disponibile in Windows. Windows Media Player non supporterà l'installazione dei tipi di carattere, quindi scegliere un tipo di carattere che si sa sarà nel sistema previsto.

Se **l'oggetto fontFace** specificato non è disponibile nel sistema dell'utente, per impostazione predefinita il controllo casella di modifica Windows tipo di carattere di sistema. Il valore predefinito per i sistemi in lingua inglese è "Tahoma". Per i sistemi internazionali, il valore predefinito viene caricato da un file di risorse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX.fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





