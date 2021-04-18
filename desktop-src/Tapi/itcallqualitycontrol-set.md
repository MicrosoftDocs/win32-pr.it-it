---
description: Il metodo set imposta il valore di una determinata proprietà del controllo di qualità della chiamata.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Metodo ITCallQualityControl:: set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328238"
---
# <a name="itcallqualitycontrolset-method"></a>Metodo ITCallQualityControl:: set

\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **set** imposta il valore di una determinata [proprietà del controllo di qualità della chiamata](callqualityproperty.md).

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

*Proprietà* \[ di in\]
</dt> <dd>

Membro dell'enumerazione [**CallQualityProperty**](callqualityproperty.md) .

</dd> <dt>

*lvalue* \[ in\]
</dt> <dd>

Valore desiderato per la proprietà.

</dd> <dt>

*è* \[ in\]
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

 

 




