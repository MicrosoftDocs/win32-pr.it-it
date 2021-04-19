---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Metodo IEnumMedia:: Clone (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333149"
---
# <a name="ienummediaclone-method"></a>Metodo IEnumMedia:: Clone

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntatore al nuovo oggetto [**IEnumMedia**](ienummedia.md) .

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

TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumMedia**](ienummedia.md) restituita da **IEnumMedia:: Clone**. L'applicazione deve chiamare **Release** sull'interfaccia **IEnumMedia** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




