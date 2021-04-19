---
description: Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Metodo ITablet2:: GetDeviceKind'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313920"
---
# <a name="itablet2getdevicekind-method"></a>Metodo ITablet2:: GetDeviceKind

Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pKind* \[ out\]
</dt> <dd>

Valore di enumerazione che indica il tipo di Tablet, ad esempio il mouse, la penna o il tocco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia e questo metodo sono stati introdotti in Windows Vista.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITablet2**](itablet2.md)
</dt> <dt>

[**Enumerazione del tipo di \_ dispositivo Tablet \_**](tablet-device-kind.md)
</dt> <dt>

[**Interfaccia ITablet**](itablet.md)
</dt> </dl>

 

 




