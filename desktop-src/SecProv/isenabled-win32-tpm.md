---
description: Il metodo IsEnabled della classe \_ Win32 Tpm indica se il dispositivo è abilitato. Questo valore può essere modificato dai metodi Enable e Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Metodo IsEnabled della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1d61c96d9c80ae77f9869261905fb93461530b452deaf7a4709b394623a3dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667501"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Metodo IsEnabled della classe \_ Win32 Tpm

Il **metodo IsEnabled** della [**classe Win32 \_ Tpm**](win32-tpm.md) indica se il dispositivo è abilitato. Questo valore può essere modificato dai [**metodi Enable**](enable-win32-tpm.md) [**e Disable.**](disable-win32-tpm.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsEnabled* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** il dispositivo è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

In base alla specifica Trusted Computing Group (TCG) v1.2, sono disponibili solo i comandi seguenti quando il dispositivo è in stato disattivato.

-   TPM \_ ContinueSelfTest
-   TPM \_ DSAP
-   TPM \_ FlushSpecific
-   TPM \_ GetCapability
-   TPM \_ GetTestResult
-   TPM \_ Init
-   TPM \_ OIAP
-   TPM \_ OSAP
-   OwnerSetDisable del TPM \_
-   Reimpostazione PCR TPM \_ \_
-   TPM \_ PhysicalDisable
-   TPM \_ PhysicalEnable
-   TPM \_ PhysicalSetDeactivated
-   Reimpostazione \_ TPM
-   TPM \_ SaveState
-   TPM \_ SelfTestFull
-   TPM \_ SetCapability
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   Avvio \_ TPM
-   Proprietà \_ TakeOwnership TPM
-   Handle di terminazione TPM \_ \_

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Abilitare**](enable-win32-tpm.md)
</dt> </dl>

 

 
