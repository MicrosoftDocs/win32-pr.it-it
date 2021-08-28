---
title: AmbientAttributes.visible
description: L'attributo visible specifica o recupera la visibilità per il controllo.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes.visible Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124051"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes.visible

**L'attributo** visible specifica o recupera la visibilità per il controllo.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                      |
|-------|----------------------------------|
| true  | Valore predefinito. Il controllo è visibile. |
| false | Il controllo non è visibile.      |



 

## <a name="remarks"></a>Commenti

Questo attributo è utile per nascondere i controlli, ad esempio quando si scambia un pulsante di sospensione per un pulsante di riproduzione.

Se il valore è false, il controllo non è visibile e gli eventi Click vengono passati al controllo dietro di esso. Se il valore è true, il controllo è visibile e riceve l'evento click stesso.

Il valore predefinito per **l'elemento AUTOMENU** è false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





