---
title: ErrorItem.condition
description: La proprietà condition recupera un valore che indica la condizione per l'errore.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem.condition Windows Media Player
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
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996641"
---
# <a name="erroritemcondition"></a>ErrorItem.condition

La **proprietà condition** recupera un valore che indica la condizione per l'errore.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di sola **lettura** (**long**) che rappresenta il codice della condizione.

## <a name="remarks"></a>Commenti

Il codice della condizione è un valore usato da Microsoft per fornire informazioni aggiuntive al personale di supporto tecnico.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





