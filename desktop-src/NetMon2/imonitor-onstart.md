---
description: Il metodo OnStart è un metodo facoltativo che può essere implementato dal monitoraggio. MCSVC chiama questo metodo per richiedere che il monitoraggio avvii l'acquisizione.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'Metodo IMonitor:: OnStart (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128323"
---
# <a name="imonitoronstart-method"></a>Metodo IMonitor:: OnStart

Il metodo **OnStart** è un metodo facoltativo che può essere implementato dal monitoraggio. MCSVC chiama questo metodo per richiedere che il monitoraggio avvii l'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnkNPP* \[ in\]
</dt> <dd>

Puntatore [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) all'interfaccia [IRTC](irtc.md) . Il monitoraggio può utilizzare questa interfaccia per ottenere statistiche che possono essere utilizzate per determinare se l'acquisizione deve essere avviata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR). Quando \_ viene restituito S OK, MCSVC chiama il metodo [IRTC:: Start](irtc-start.md) .

Se il metodo ha esito negativo, il valore restituito è un codice di errore. Il MCSVC non avvierà l'acquisizione se viene restituito un codice di errore.

## <a name="remarks"></a>Commenti

MCSVC chiama questo metodo prima di chiamare il metodo [IRTC:: Start](irtc-start.md) di NPP per avviare l'acquisizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IMonitor](imonitor.md)
</dt> <dt>

[Provider di pacchetti di rete](network-packet-providers.md)
</dt> </dl>

 

