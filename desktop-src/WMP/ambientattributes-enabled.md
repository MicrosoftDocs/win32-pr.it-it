---
title: AmbientAttributes.enabled
description: L'attributo enabled specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes.enabled Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d8e000d64ef92212cd7c6cf37c7fd79036107e1d3be0d7669d73b40c759de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055179"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes.enabled

**L'attributo** enabled specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione               |
|-------|---------------------------|
| true  | Valore predefinito. Controllo abilitato. |
| false | Controllo disabilitato.         |



 

## <a name="remarks"></a>Commenti

Se il controllo è abilitato, può avere una tabulazione e riceverà tutti gli eventi di ambiente. Se disabilitato, il controllo non dispone di una tabulazione e non riceve eventi di ambiente del mouse o della tastiera generati. Tuttavia, continuerà a ricevere tutti gli altri eventi di ambiente generati.

Questo attributo non è supportato per **l'elemento SUBVIEW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





