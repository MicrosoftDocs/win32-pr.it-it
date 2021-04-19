---
title: EFFETTI. finestra
description: L'attributo windowd specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ovvero se l'intero rettangolo del controllo sarà visibile in qualsiasi momento o se può essere ritagliato.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFETTI. finestre Media Player finestra
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333411"
---
# <a name="effectswindowed"></a>EFFETTI. finestra

L'attributo **windowd** specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ovvero se l'intero rettangolo del controllo sarà visibile in qualsiasi momento o se può essere ritagliato. Questo attributo può essere impostato solo in fase di progettazione.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura in seguito.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| true  | Il controllo sarà finestra.            |
| false | Valore predefinito. Il controllo sarà privo di finestra. |



 

## <a name="remarks"></a>Commenti

Se si desidera una finestra di visualizzazione non rettangolare o se una parte della finestra è coperta da un'immagine, questo attributo deve essere impostato su false. In questo modo si sacrificano alcune prestazioni per eseguire il troncamento necessario.

Se **la finestra è** impostata su true, qualsiasi immagine che copre la finestra di visualizzazione viene ignorata e la finestra di visualizzazione dispone dell'ordine z di livello più alto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> </dl>

 

 





