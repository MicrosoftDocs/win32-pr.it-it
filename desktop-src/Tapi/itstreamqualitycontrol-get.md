---
description: Il metodo Get recupera il valore di una determinata proprietà di qualità del flusso.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: Metodo ITStreamQualityControl::Get (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a82a448320115664ab0664c2f7d8cde9f8049c7ee2cb86ccf7e46f856ceafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080501"
---
# <a name="itstreamqualitycontrolget-method"></a>Metodo ITStreamQualityControl::Get

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Get** recupera il valore di una determinata proprietà di qualità del [**flusso**](streamqualityproperty.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione StreamQualityProperty.**](streamqualityproperty.md)

</dd> <dt>

*plValue* \[ Cambio\]
</dt> <dd>

Valore della proprietà *di* input .

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

[**Proprietà StreamQuality**](streamqualityproperty.md)
</dt> </dl>

 

 




