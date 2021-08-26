---
description: Recupera lo stato NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: Metodo IESP::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 00b83cbbb167775a8de360c880f381b41f250abf0eab01c883bc7580be4d956f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037541"
---
# <a name="iespquerystatus-method"></a>Metodo IESP::QueryStatus

Il **metodo QueryStatus** recupera lo stato NPP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNetworkStatus* \[ Cambio\]
</dt> <dd>

Puntatore a una struttura [NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del NPP. L'utente deve allocare e liberare la memoria per la struttura NETWORKSTATUS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PARAMETRO NON VALIDO DI \_ \_ NMERR**</dt> </dl> | Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida. Allocare memoria per questa struttura e chiamare **di nuovo IESP::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo [la chiamata a CreateNPPInterface.](createnppinterface.md) È possibile chiamare questo metodo per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono presenti trigger in sospeso.

Prima di chiamare questo metodo, allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




