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
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306406"
---
# <a name="disable-method-of-the-win32_tpm-class"></a>Metodo Disable della \_ classe TPM Win32

Il metodo **Disable** della classe [**\_ TPM Win32**](win32-tpm.md) consente al proprietario del TPM di disabilitare o sospendere il TPM. Questo metodo sospende BitLocker se la chiamata a può causare la richiesta del ripristino BitLocker. BitLocker verrà ripreso automaticamente dopo il provisioning del TPM.

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

Stringa che identifica il proprietario del TPM. Questa stringa deve essere una stringa con codifica Base64 che contiene esattamente 20 byte di dati binari. Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto. Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | Il valore di autorizzazione del proprietario specificato non è in grado di eseguire la richiesta.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout. Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Commenti

Per disabilitare il TPM senza avere il valore di autorizzazione del proprietario del TPM, usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
