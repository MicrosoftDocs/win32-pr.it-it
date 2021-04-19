---
title: TESTO. fontSmoothing
description: L'attributo fontSmoothing specifica o recupera un valore che indica se la smussatura dei caratteri è abilitata.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Media Player di Windows TEXT. fontSmoothing
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325118"
---
# <a name="textfontsmoothing"></a>TESTO. fontSmoothing

L'attributo **fontSmoothing** specifica o recupera un valore che indica se la smussatura dei caratteri è abilitata.

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                          |
|-------|--------------------------------------|
| true  | La smussatura dei caratteri è abilitata.           |
| false | Valore predefinito. La smussatura dei caratteri è disabilitata. |



 

## <a name="remarks"></a>Commenti

La smussatura dei caratteri usa la funzionalità di anti-aliasing del sistema operativo. Se la smussatura dei caratteri è abilitata e il sistema operativo supporta l'anti-aliasing, Windows Media Player tenta di smussare il testo. Non tutti i tipi di carattere supportano l'anti-aliasing. Windows Media Player 10 usa il metodo di anti-aliasing di Windows XP ClearType.

-   **Avviso** di La smussatura dei caratteri su un colore trasparente può causare la fusione del colore trasparente nei caratteri. Non è consigliabile usare **fontSmoothing** se il testo verrà visualizzato su una trasparenza.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





