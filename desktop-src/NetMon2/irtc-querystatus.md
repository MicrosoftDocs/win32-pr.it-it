---
description: 'Metodo IRTC::QueryStatus: il metodo QueryStatus recupera lo stato del NPP.'
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: Metodo IRTC::QueryStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd8c18d19df7d577ad219742520630f00122a41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110609"
---
# <a name="irtcquerystatus-method"></a>Metodo IRTC::QueryStatus

Il **metodo QueryStatus** recupera lo stato del NPP.

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

Puntatore a una [struttura NETWORKSTATUS](networkstatus.md) restituita che indica lo stato corrente (acquisizione, sospensione, arresto e così via) del NPP. È responsabilità dell'applicazione allocare e liberare la memoria per la **struttura NETWORKSTATUS.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è il codice di errore seguente:



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PARAMETRO NON VALIDO DI \_ NMERR \_**</dt> </dl> | Il *parametro pNetworkStatus* non punta a una struttura [NETWORKSTATUS](networkstatus.md) valida. Allocare memoria per questa struttura e chiamare **di nuovo IRTC::QueryStatus.**<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere chiamato in qualsiasi momento dopo [la chiamata del metodo CreateNPPInterface.](createnppinterface.md) È possibile chiamare questo metodo per verificare se il NPP è connesso alla rete, per individuare lo stato dell'acquisizione corrente e per verificare se sono presenti trigger in sospeso. Prima di chiamare questo metodo, tuttavia, è necessario allocare la memoria necessaria per la struttura [NETWORKSTATUS](networkstatus.md) e liberare tale memoria quando la struttura non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




