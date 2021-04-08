---
description: Installa un proprietario per il TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Metodo TakeOwnership della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058180"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Metodo TakeOwnership della \_ classe TPM Win32

Il metodo **TakeOwnership** della classe [**\_ TPM Win32**](win32-tpm.md) installa un proprietario per il TPM. Il proprietario del TPM può avvalersi completamente delle funzionalità TPM. Dopo aver impostato un proprietario, nessun altro utente o software può richiedere la proprietà del TPM.

I metodi [**IsEnabled**](isenabled-win32-tpm.md), IsEnabled [**e**](isactivated-win32-tpm.md) [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devono essere tutti true prima che il metodo **TakeOwnership** possa avere esito positivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica il proprietario del TPM. Questa stringa deve essere una stringa con codifica Base64 con terminazione null che contiene esattamente 20 byte di dati binari. Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per tradurre una passphrase nel formato previsto. Il parametro *OwnerAuth* viene letto dal registro di sistema se non ne viene specificato alcuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Il parametro *OwnerAuth* non è valido.<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_ E \_ owner \_ set**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | Un proprietario esiste già nel TPM.<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ Nessuna \_**</dt> verifica dell'autenticità <dt>2150105123 (0x80280023)</dt> </dl>       | Non è possibile trovare la chiave di verifica dell'autenticità nel TPM.<br/> Per creare una coppia di chiavi di verifica dell'autenticità nel TPM, vedere il metodo [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .<br/>             |
| <dl> <dt>**TPM \_ E \_ installazione \_ disabilitata**</dt> <dt>2150105099 (0x8028000B)</dt> </dl>     | Non è possibile installare un proprietario in questo TPM.<br/> Per informazioni su come consentire l'installazione del proprietario di un dispositivo, vedere [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout. Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                               |



 

## <a name="remarks"></a>Commenti

I metodi [**IsEnabled, IsEnabled**](isenabled-win32-tpm.md)e [](isactivated-win32-tpm.md) [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devono essere tutti true prima che **TakeOwnership** possa avere esito positivo.

È necessario usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per modificare una passphrase nel valore di input usato per il parametro *OwnerAuth* .

Il metodo **TakeOwnership** esegue il backup del valore di autorizzazione del proprietario per Active Directory se sono state configurate le impostazioni criteri di gruppo appropriate.

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

 

 
