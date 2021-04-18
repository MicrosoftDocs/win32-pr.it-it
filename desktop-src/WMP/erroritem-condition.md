---
title: ErrorItem. Condition
description: La proprietà Condition recupera un valore che indica la condizione per l'errore.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- Media Player di Windows ErrorItem. Condition
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331585"
---
# <a name="erroritemcondition"></a>ErrorItem. Condition

La proprietà **Condition** recupera un valore che indica la condizione per l'errore.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di sola lettura (**Long**) che rappresenta il codice della condizione.

## <a name="remarks"></a>Commenti

Il codice della condizione è un valore utilizzato da Microsoft per fornire informazioni aggiuntive per il personale del supporto tecnico.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





