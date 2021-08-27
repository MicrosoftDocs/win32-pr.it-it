---
description: Il metodo IsOwnerClearDisabled della classe Win32 Tpm indica se al proprietario del dispositivo è limitata la \_ cancellazione del dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Metodo IsOwnerClearDisabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 639804b21c97a6e445c0eddc9253c46774a4ccd895d58bfe32289432702cbe03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080631"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a>Metodo IsOwnerClearDisabled della classe Tpm Win32 \_

Il **metodo IsOwnerClearDisabled** della classe [**\_ Win32 Tpm**](win32-tpm.md) indica se al proprietario del dispositivo è limitata la cancellazione del dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsOwnerClearDisabled* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** il proprietario del dispositivo non è in grado di cancellare il dispositivo. Solo un utente fisicamente presente può essere in grado di cancellare il dispositivo. Se **false,** il proprietario del dispositivo è in grado di cancellare il dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
