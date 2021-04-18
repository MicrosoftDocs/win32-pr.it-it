---
description: Il metodo GetRange Ottiene l'intervallo di valori validi per una determinata proprietà di qualità del flusso.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'Metodo ITStreamQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328592"
---
# <a name="itstreamqualitycontrolgetrange-method"></a>Metodo ITStreamQualityControl:: GetRange

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **GetRange** Ottiene l'intervallo di valori validi per una determinata [**proprietà di qualità del flusso**](streamqualityproperty.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ di in\]
</dt> <dd>

Membro dell'enumerazione [**StreamQualityProperty**](streamqualityproperty.md) .

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

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




