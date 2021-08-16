---
description: Il metodo GetRange ottiene l'intervallo di valori validi per una determinata proprietà di qualità della chiamata.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: Metodo ITCallQualityControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d21c9266e64a9bcb31da0028a0ea28b8de98793d56d5bcf28c791c5497756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762437"
---
# <a name="itcallqualitycontrolgetrange-method"></a>Metodo ITCallQualityControl::GetRange

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo GetRange** ottiene l'intervallo di valori validi per una determinata proprietà [di qualità della chiamata.](callqualityproperty.md)

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

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione CallQualityProperty.**](callqualityproperty.md)

</dd> <dt>

*plMin* \[ Cambio\]
</dt> <dd>

Valore minimo valido per la proprietà di input.

</dd> <dt>

*plMax* \[ Cambio\]
</dt> <dd>

Valore massimo valido per la proprietà di input.

</dd> <dt>

*plSteppingDelta* \[ Cambio\]
</dt> <dd>

Incremento in base al quale il valore della proprietà può essere aumentato o diminuito.

</dd> <dt>

*plDefault* \[ Cambio\]
</dt> <dd>

Valore predefinito per il *parametro Property.*

</dd> <dt>

*plFlags* \[ Cambio\]
</dt> <dd>

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come viene *controllato il valore* di Property.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




