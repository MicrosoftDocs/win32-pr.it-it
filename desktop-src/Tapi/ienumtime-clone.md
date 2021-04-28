---
description: 'Metodo IEnumTime::Clone: il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: Metodo IEnumTime::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090739"
---
# <a name="ienumtimeclone-method"></a>Metodo IEnumTime::Clone

\[ Le interfacce e i controlli di conferenza di telefonia IP di Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ Cambio\]
</dt> <dd>

Puntatore al nuovo [**oggetto IEnumTime.**](ienumtime.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppEnum* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Operazione non riuscita per motivi sconosciuti.<br/>                          |



 

## <a name="remarks"></a>Commenti

TAPI chiama il **metodo AddRef** sull'interfaccia [**IEnumTime**](ienumtime.md) restituita da **IEnumTime::Clone.** L'applicazione deve **chiamare Release** **sull'interfaccia IEnumTime** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




