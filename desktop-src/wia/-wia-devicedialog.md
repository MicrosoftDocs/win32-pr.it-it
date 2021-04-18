---
description: Utilizzato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Funzione DeviceDialog (Wiadevd. h)
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
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312442"
---
# <a name="devicedialog-function"></a>DeviceDialog (funzione)

Utilizzato dalle applicazioni per visualizzare una finestra di dialogo del dispositivo all'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDeviceDialogData* \[ in\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA**

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) da usare per creare la finestra di dialogo del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




