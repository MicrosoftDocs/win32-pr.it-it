---
description: Il metodo GetRange Ottiene l'intervallo di valori validi per una determinata proprietà della qualità della chiamata.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'Metodo ITCallQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328058"
---
# <a name="itcallqualitycontrolgetrange-method"></a>Metodo ITCallQualityControl:: GetRange

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetRange** Ottiene l'intervallo di valori validi per una determinata [proprietà della qualità della chiamata](callqualityproperty.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ di in\]
</dt> <dd>

Membro dell'enumerazione [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Valore minimo valido per la proprietà di input.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Valore valido massimo per la proprietà di input.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Incremento in base al quale è possibile aumentare o diminuire il valore della proprietà.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Valore predefinito per il parametro *Property* .

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valore dell'enumerazione [**TAPIControlFlags**](tapicontrolflags.md) che indica la modalità di controllo del valore della *Proprietà* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




