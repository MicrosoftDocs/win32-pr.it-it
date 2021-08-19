---
description: 'Metodo IEnumTime::Skip: il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: Metodo IEnumTime::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36f92ead711c25b385c2a7109dbb113b8c5ca082fda9c3012204384350a3c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762950"
---
# <a name="ienumtimeskip-method"></a>Metodo IEnumTime::Skip

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                             | Descrizione                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Il numero di elementi ignorati è *celt*.<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Number of elements skipped was not *celt*.<br/> |



 

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

 

 




