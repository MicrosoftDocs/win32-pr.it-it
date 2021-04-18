---
description: Il metodo OnStop deve essere implementato dal monitoraggio. MSCVC chiama questo metodo per notificare al monitoraggio che l'acquisizione verrà arrestata.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Metodo IMonitor:: OnStop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305871"
---
# <a name="imonitoronstop-method"></a>Metodo IMonitor:: OnStop

Il metodo **OnStop** deve essere implementato dal monitoraggio. MSCVC chiama questo metodo per notificare al monitoraggio che l'acquisizione verrà arrestata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR).

Se il metodo ha esito negativo, il valore restituito è un codice di errore. Quando viene restituito un codice di errore, il monitoraggio non può essere riavviato.

## <a name="remarks"></a>Commenti

MCSVC chiama questo metodo dopo la chiamata a [IRTC:: Stop](irtc-stop.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




