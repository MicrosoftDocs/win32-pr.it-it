---
title: EFFECTs. allowAll
description: L'attributo allowAll specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel registro di sistema.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTs. allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325859"
---
# <a name="effectsallowall"></a>EFFECTs. allowAll

L'attributo **allowAll** specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel registro di sistema.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                         |
|-------|---------------------------------------------------------------------|
| true  | Valore predefinito. Consente il ciclo di tutte le visualizzazioni nel sistema dell'utente. |
| false | Limita il ciclo alle visualizzazioni visualizzate all'interno dei tag **degli effetti** . |



 

## <a name="remarks"></a>Commenti

Se questo attributo è impostato su false, solo le visualizzazioni visualizzate all'interno dei tag **Effects** possono essere ciclate usando Previous/Next. Se è impostato su true, tutte le visualizzazioni registrate nel sistema dell'utente possono essere ciclate tramite. Se è impostato su true e si specificano le visualizzazioni all'interno dei tag **Effects** , gli attributi specificati in questi tag vengono applicati a tutte le visualizzazioni nel sistema dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> </dl>

 

 





