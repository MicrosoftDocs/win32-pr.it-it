---
description: Il metodo GetRange ottiene l'intervallo di valori validi per una determinata proprietà di qualità del flusso.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: Metodo ITStreamQualityControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13d07b848ef3be744f40ec1ba4bb4a73514f88204fa1918db661e00d36019ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774471"
---
# <a name="itstreamqualitycontrolgetrange-method"></a>Metodo ITStreamQualityControl::GetRange

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo GetRange** ottiene l'intervallo di valori validi per una determinata proprietà [**di qualità del flusso.**](streamqualityproperty.md)

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

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione StreamQualityProperty.**](streamqualityproperty.md)

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

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come viene *controllato il valore* della proprietà.

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

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**Proprietà StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




