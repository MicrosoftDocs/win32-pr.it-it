---
title: AmbientAttributes. Enabled
description: L'attributo enabled specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- Media Player Windows AmbientAttributes. Enabled
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324753"
---
# <a name="ambientattributesenabled"></a>AmbientAttributes. Enabled

L'attributo **Enabled** specifica o recupera un valore che indica se il controllo è abilitato o disabilitato.

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione               |
|-------|---------------------------|
| true  | Valore predefinito. Controllo abilitato. |
| false | Controllo disabilitato.         |



 

## <a name="remarks"></a>Commenti

Se il controllo è abilitato, può avere una tabulazione e riceverà tutti gli eventi di ambiente. Quando è disabilitato, il controllo non ha una tabulazione e non riceve alcun evento mouse o tastiera di ambiente attivato. Continuerà comunque a ricevere tutti gli altri eventi di ambiente generati.

Questo attributo non è supportato per l'elemento di **visualizzazione** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





