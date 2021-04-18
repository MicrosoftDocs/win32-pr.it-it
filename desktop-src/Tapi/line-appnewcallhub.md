---
description: Il messaggio della linea TAPI \_ APPNEWCALLHUB viene inviato per informare un'applicazione quando è stato creato un nuovo hub di chiamata.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Messaggio di LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331033"
---
# <a name="line_appnewcallhub-message"></a>\_Messaggio linea APPNEWCALLHUB

Il messaggio della **linea TAPI \_ APPNEWCALLHUB** viene inviato per informare un'applicazione quando è stato creato un nuovo hub di chiamata.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle della chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Livello di rilevamento sul nuovo hub, come definito da una delle [**\_ costanti LINECALLHUBTRACKING**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio ha origine con TAPI anziché con un provider di servizi, pertanto non esiste alcun messaggio TSPI corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




