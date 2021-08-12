---
description: Usato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Funzione DeviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: de8a3d36472d51c24a2c007ad7be0be371a0b5d8bb39e75f457e204250e8f53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441679"
---
# <a name="devicedialog-function"></a>Funzione DeviceDialog

Usato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ Pollici\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA**

[**DEVICEDIALOGDATA da**](-wia-devicedialogdata.md) usare per creare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




