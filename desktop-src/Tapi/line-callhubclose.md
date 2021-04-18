---
description: Il messaggio della linea TAPI \_ CALLHUBCLOSE viene inviato quando un hub di chiamata è stato chiuso.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Messaggio di LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328053"
---
# <a name="line_callhubclose-message"></a>\_Messaggio linea CALLHUBCLOSE

Il messaggio della **linea TAPI \_ CALLHUBCLOSE** viene inviato quando un hub di chiamata è stato chiuso.


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

Riservato. Impostare su 0.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Riservato. Impostare su 0.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Impostare su 0.

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



 

 




