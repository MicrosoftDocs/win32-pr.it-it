---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Metodo IEnumTime:: Clone (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332256"
---
# <a name="ienumtimeclone-method"></a>Metodo IEnumTime:: Clone

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntatore al nuovo oggetto [**IEnumTime**](ienumtime.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppEnum* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>  | Operazione non riuscita per motivi sconosciuti.<br/>                          |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumTime**](ienumtime.md) restituita da **IEnumTime:: Clone**. L'applicazione deve chiamare **Release** sull'interfaccia **IEnumTime** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




