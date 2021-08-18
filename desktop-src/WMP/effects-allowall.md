---
title: EFFECTS.allowAll
description: L'attributo allowAll specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel Registro di sistema.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- EFFECTS.allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a87aa8336e3961b31716c8d6bbfaa6aee71374a0f3c6e17b644a47136df550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996847"
---
# <a name="effectsallowall"></a>EFFECTS.allowAll

**L'attributo allowAll** specifica o recupera un valore che indica se includere tutte le visualizzazioni presenti nel Registro di sistema.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                                         |
|-------|---------------------------------------------------------------------|
| true  | Valore predefinito. Consente il ciclo di tutte le visualizzazioni nel sistema dell'utente. |
| false | Limita il ciclo alle visualizzazioni visualizzate all'interno **dei tag EFFECTS.** |



 

## <a name="remarks"></a>Commenti

Se questo attributo è impostato su false, è possibile scorrere solo le visualizzazioni visualizzate all'interno dei tag **EFFECTS** usando previous/next. Se è impostato su true, è possibile scorrere tutte le visualizzazioni registrate nel sistema dell'utente. Se è impostato su true e si specificano visualizzazioni all'interno dei tag **EFFECTS,** gli attributi specificati in questi tag vengono applicati a tutte le visualizzazioni nel sistema dell'utente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> </dl>

 

 





