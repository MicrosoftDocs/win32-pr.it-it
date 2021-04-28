---
description: 'Metodo IEnumTime::Skip: il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione.'
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: Metodo IEnumTime::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190a98c14cb8f551276a173e2d73872d876f2ceb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090719"
---
# <a name="ienumtimeskip-method"></a>Metodo IEnumTime::Skip

\[ I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

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
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Il numero di elementi ignorati non è *stato cel*.<br/> |



 

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

 

 




