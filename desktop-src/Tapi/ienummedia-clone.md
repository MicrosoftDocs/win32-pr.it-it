---
description: 'Metodo IEnumMedia::Clone: il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: Metodo IEnumMedia::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894457684e94d07426511979dcb40cfcbbe75ed9fec91e024f09175389261620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992441"
---
# <a name="ienummediaclone-method"></a>Metodo IEnumMedia::Clone

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* \[ Cambio\]
</dt> <dd>

Puntatore al nuovo [**oggetto IEnumMedia.**](ienummedia.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro ppEnum* non è un puntatore valido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>  | Operazione non riuscita per motivi sconosciuti.<br/>                          |



 

## <a name="remarks"></a>Commenti

TAPI chiama il **metodo AddRef** [**sull'interfaccia IEnumMedia**](ienummedia.md) restituita da **IEnumMedia::Clone**. L'applicazione deve **chiamare Release** **sull'interfaccia IEnumMedia** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




