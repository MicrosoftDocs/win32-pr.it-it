---
title: EFFECTS.windowed
description: L'attributo windowed specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ad esempio se l'intero rettangolo del controllo sarà sempre visibile o se può essere ritagliato.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFECTS.windowed Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651001"
---
# <a name="effectswindowed"></a>EFFECTS.windowed

L'attributo **windowed** specifica o recupera un valore che indica se la visualizzazione sarà finestra o senza finestra, ad esempio se l'intero rettangolo del controllo sarà sempre visibile o se può essere ritagliato. Questo attributo può essere impostato solo in fase di progettazione.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura successivamente.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| true  | Il controllo verrà visualizzato in una finestra.            |
| false | Valore predefinito. Il controllo sarà senza finestra. |



 

## <a name="remarks"></a>Commenti

Se si desidera una finestra di visualizzazione non rettangolare o se una parte qualsiasi della finestra è coperta da un'immagine, questo attributo deve essere impostato su false. Ciò consente di sacrificare alcune prestazioni per eseguire il ritaglio necessario.

Se **windowed** è impostato su true, qualsiasi immagine che copre la finestra di visualizzazione viene ignorata e la finestra di visualizzazione ha l'ordine z di livello più alto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> </dl>

 

 





