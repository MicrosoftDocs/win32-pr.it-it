---
description: Abilita o Disabilita la lettura e la scrittura dei settori del disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW (funzione)
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
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877546"
---
# <a name="fveenablerawaccessw-function"></a>FveEnableRawAccessW (funzione)

Abilita o Disabilita la lettura e la scrittura dei settori del disco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeName* \[ in\]
</dt> <dd>

Identificatore univoco del volume del disco.

</dd> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Se **true**, consente l'accesso al volume non elaborato. Se **false**, non è consentito l'accesso al volume non elaborato. Se l'accesso non elaborato è già stato abilitato ma questo valore è **false**, il volume viene rimontato e riconvalidato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                           | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | La funzione è stata completata.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Enabled è **false** e il volume non è già in modalità di accesso non elaborato.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | Il volume non può essere bloccato.<br/>                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




