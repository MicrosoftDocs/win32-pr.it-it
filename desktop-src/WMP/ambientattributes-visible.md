---
title: AmbientAttributes. Visible
description: L'attributo Visible specifica o recupera la visibilità per il controllo.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes. Visible Media Player Windows
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331498"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes. Visible

L'attributo **Visible** specifica o recupera la visibilità per il controllo.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                      |
|-------|----------------------------------|
| true  | Valore predefinito. Il controllo è visibile. |
| false | Il controllo non è visibile.      |



 

## <a name="remarks"></a>Commenti

Questo attributo è utile per nascondere i controlli, ad esempio quando si scambia un pulsante di sospensione per un pulsante Riproduci.

Se il valore è false, il controllo non è visibile e gli eventi click vengono passati al controllo sottostante. Se il valore è true, il controllo è visibile e riceve l'evento Click stesso.

Il valore predefinito per l'elemento **automenu** è false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





