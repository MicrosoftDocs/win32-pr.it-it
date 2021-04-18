---
title: ErrorItem. errorContext
description: La proprietà errorContext recupera un valore che indica il contesto dell'errore.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Media Player Windows ErrorItem. errorContext
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324742"
---
# <a name="erroritemerrorcontext"></a>ErrorItem. errorContext

La proprietà **errorContext** recupera un valore che indica il contesto dell'errore.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura che rappresenta il codice del contesto dell'errore.

## <a name="remarks"></a>Commenti

Il contesto di errore è costituito dalle informazioni utilizzate da Microsoft per fornire informazioni aggiuntive per il personale del supporto tecnico.

**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





