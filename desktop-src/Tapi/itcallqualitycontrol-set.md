---
description: Il metodo Set imposta il valore di una determinata proprietà del controllo qualità delle chiamate.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: Metodo ITCallQualityControl::Set (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5506e4c318440c2b611a2404590bdf638d34a7da2353a5598d09aecf2990668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003389"
---
# <a name="itcallqualitycontrolset-method"></a>Metodo ITCallQualityControl::Set

\[Questo metodo non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Set** imposta il valore di una determinata proprietà del controllo qualità delle [chiamate.](callqualityproperty.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Proprietà* \[ Pollici\]
</dt> <dd>

Membro [**dell'enumerazione CallQualityProperty.**](callqualityproperty.md)

</dd> <dt>

*lValue* \[ Pollici\]
</dt> <dd>

Valore desiderato per la proprietà.

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione TAPIControlFlags**](tapicontrolflags.md) che indica come *deve* essere controllato il valore della proprietà.

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

 

 




