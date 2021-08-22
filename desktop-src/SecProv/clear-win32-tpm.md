---
description: Reimposta lo stato predefinito del TPM.
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
ms.openlocfilehash: c9c3185fceb315cf9c36caa7de1e450820ad25ce1b31fefc8135c4d57fd76597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892648"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Metodo Clear della classe Tpm Win32 \_

Il **metodo Clear** della classe [**\_ Tpm Win32**](win32-tpm.md) reimposta il TPM sullo stato predefinito della factory. Un proprietario del TPM può usare questo metodo per annullare la proprietà del TPM e invalidare i materiali crittografici creati dal proprietario precedente. Questo metodo sospende BitLocker se la chiamata può causare la necessità del ripristino di BitLocker. BitLocker riprenderà automaticamente dopo il provisioning del TPM.

> [!Caution]  
> Cancellando il TPM, si perderanno tutte le chiavi TPM create e usate dalle applicazioni. Se queste chiavi sono state usate per crittografare i dati, assicurarsi di avere un altro modo per accedere ai dati prima di cancellare il TPM.

 

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

L'esecuzione di questo metodo consente di preparare un computer dotato di TPM per il riciclo.

Per cancellare il TPM ma non avere più l'autorizzazione del proprietario del TPM, è necessario l'accesso fisico al computer. Il [**metodo SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) include funzionalità che consentono di cancellare il TPM senza autorizzazione del proprietario TPM.

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

 

 
