---
description: Reimposta il TPM sullo stato predefinito della factory.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Metodo Clear della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232930"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Metodo Clear della \_ classe TPM Win32

Il metodo **Clear** della classe [**\_ TPM Win32**](win32-tpm.md) Reimposta il TPM sullo stato predefinito della factory. Un proprietario del TPM può utilizzare questo metodo per annullare la proprietà del TPM e invalidare i materiali crittografici creati dal proprietario precedente. Questo metodo sospende BitLocker se la chiamata a può causare la richiesta del ripristino BitLocker. BitLocker verrà ripreso automaticamente dopo il provisioning del TPM.

> [!Caution]  
> Deselezionando il TPM, si perderanno tutte le chiavi TPM create e utilizzate dalle applicazioni. Se queste chiavi sono state usate per crittografare i dati, assicurarsi di disporre di un altro modo per accedere ai dati prima di cancellare il TPM.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 Clear(
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

L'esecuzione di questo metodo consente di preparare un computer dotato di TPM per il riciclo.

Per cancellare il TPM ma che non dispone più dell'autorizzazione del proprietario del TPM, è necessario l'accesso fisico al computer. Il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) include funzionalità che consentono di cancellare il TPM senza autorizzazione del proprietario del TPM.

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
</dt> </dl>

 

 
