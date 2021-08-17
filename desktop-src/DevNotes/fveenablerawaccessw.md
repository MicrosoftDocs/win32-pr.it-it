---
description: Abilita o disabilita la lettura e la scrittura di settori del disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Funzione FveEnableRawAccessW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956090"
---
# <a name="fveenablerawaccessw-function"></a>Funzione FveEnableRawAccessW

Abilita o disabilita la lettura e la scrittura di settori del disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeName* \[ Pollici\]
</dt> <dd>

Identificatore univoco per il volume del disco.

</dd> <dt>

*Abilitato* \[ Pollici\]
</dt> <dd>

Se **TRUE,** consente l'accesso al volume non elaborato. Se **FALSE,** non è consentito l'accesso al volume non elaborato. Se l'accesso non elaborato è già stato abilitato ma questo valore **è FALSE,** il volume viene rimontaggio e riconvalida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                           | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | La funzione ha avuto esito positivo.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Enabled è **FALSE** e il volume non era già in modalità di accesso non elaborato.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | Il volume non può essere bloccato.<br/>                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




