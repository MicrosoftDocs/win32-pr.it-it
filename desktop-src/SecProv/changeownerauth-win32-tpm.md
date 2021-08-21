---
description: Modifica il valore di autorizzazione del proprietario del TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Metodo ChangeOwnerAuth della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004679"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Metodo ChangeOwnerAuth della classe Tpm Win32 \_

Il **metodo ChangeOwnerAuth** della classe [**\_ Win32 Tpm**](win32-tpm.md) modifica il valore di autorizzazione del proprietario del TPM.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldOwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che indica il valore di autorizzazione del proprietario del TPM corrente del dispositivo. Usare il [**metodo ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione. Il *parametro OldOwnerAuth* non viene fornito o viene fornita una stringa vuota. Questo metodo ottiene il valore dal Registro di sistema, se presente.

</dd> <dt>

*NewOwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che specifica il nuovo valore di autorizzazione del proprietario del TPM. Usare il [**metodo ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione. Il *parametro NewOwnerAuth* non può essere vuoto o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | Il valore di autorizzazione del proprietario del TPM corrente non è corretto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ DEFEND \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | Il TPM è in difesa dagli attacchi con dizionario ed è in un periodo di timeout. Per altre informazioni, vedere il [**metodo ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ SCHEMA DI ACTIVE DIRECTORY \_ \_ \_ NON**</dt> <dt>INSTALLATO 2150694922 (0x8031000A)</dt> </dl> | Impossibile salvare le informazioni di ripristino nella rete. Il computer è stato configurato per archiviare le informazioni di ripristino Active Directory Domain Services. Per istruzioni su come configurare Active Directory, vedere Guida alla configurazione di Crittografia unità BitLocker: Backup di BitLocker e delle informazioni di [ripristino TPM in Active Directory.](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))<br/> |
| <dl> <dt>**Connessione non**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | Impossibile salvare le informazioni di ripristino nella rete. Il computer è stato configurato per archiviare le informazioni di ripristino Active Directory Domain Services. Per continuare, è necessaria una connessione di rete.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il **metodo ChangeOwnerAuth** esegue il backup della nuova autorizzazione del proprietario del TPM Active Directory Domain Services se sono state configurate le impostazioni Criteri di gruppo appropriate.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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
</dt> </dl>

 

 
