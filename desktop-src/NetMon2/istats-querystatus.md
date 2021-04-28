---
description: 'Metodo IStats::QueryStatus: il metodo QueryStatus recupera lo stato di NPP.'
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: Metodo IStats::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7587c2fff56d305c0298948bdf8690fd801f3f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113479"
---
# <a name="istatsquerystatus-method"></a>Metodo IStats::QueryStatus

Il **metodo QueryStatus** recupera lo stato di NPP.

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

Puntatore a una struttura [NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del servizio NPP. È responsabilità dell'applicazione allocare e liberare la memoria per la **struttura NETWORKSTATUS.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PARAMETRO NON \_ VALIDO DI NMERR \_**</dt> </dl> | Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida. Allocare memoria per questa struttura e chiamare nuovamente il **metodo IStats::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo la [chiamata del metodo CreateNPPInterface.](createnppinterface.md) Può essere chiamato per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono in sospeso trigger. Prima di chiamare questo metodo, tuttavia, è necessario allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




