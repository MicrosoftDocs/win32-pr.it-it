---
description: Consente al proprietario del TPM di disabilitare o sospendere il TPM.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Metodo Disable della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a2bd76795cceaf299843b0b47f6f798d4471c67241f7c3fa206db52060bde745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668041"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Metodo Disable della classe Tpm Win32 \_

Il **metodo Disable** della classe [**\_ Tpm Win32**](win32-tpm.md) consente al proprietario del TPM di disabilitare o sospendere il TPM. Questo metodo sospende BitLocker se la chiamata può causare la necessità del ripristino di BitLocker. BitLocker riprenderà automaticamente dopo il provisioning del TPM.

## <a name="syntax"></a>Sintassi


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica il proprietario del TPM. Questa stringa deve essere una stringa con codifica Base64 che contiene esattamente 20 byte di dati binari. Usare il [**metodo ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una passphrase nel formato previsto. Il *parametro OwnerAuth* viene letto dal Registro di sistema se non ne viene fornito nessuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | Il valore di autorizzazione del proprietario specificato non può eseguire la richiesta.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFEND LOCK RUNNING \_ \_ 2150107139**</dt> <dt>(0x80280803)</dt> </dl> | Il TPM si sta difendendo dagli attacchi di dizionario ed è in un periodo di timeout. Per altre informazioni, vedere il [**metodo ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Commenti

Per disabilitare il TPM senza avere il valore di autorizzazione del proprietario TPM, usare il [**metodo SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md)

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
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
