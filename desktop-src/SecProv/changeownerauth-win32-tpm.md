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
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128759"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Metodo ChangeOwnerAuth della \_ classe TPM Win32

Il metodo **ChangeOwnerAuth** della classe [**\_ TPM Win32**](win32-tpm.md) modifica il valore di autorizzazione del proprietario del TPM.

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

Tipo: **stringa**

Stringa che assegna un nome al valore di autorizzazione corrente del proprietario del TPM del dispositivo. Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione. Il parametro *OldOwnerAuth* non è specificato o viene specificata una stringa vuota, questo metodo ottiene il valore dal registro di sistema, se presente.

</dd> <dt>

*NewOwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che assegna un nome al nuovo valore di autorizzazione del proprietario del TPM. Usare il metodo [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una password in questo valore di autorizzazione. Il parametro *NewOwnerAuth* non può essere vuoto o **null.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | Il valore di autorizzazione del proprietario del TPM corrente non è corretto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ difendono il \_ blocco \_ che esegue**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | Il TPM è in difesa dagli attacchi del dizionario e si trova in un periodo di timeout. Per ulteriori informazioni, vedere il metodo [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ \_Schema di ad E \_ \_ non \_ installato**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | Non è possibile salvare le informazioni di ripristino nella rete. Il computer è stato configurato per archiviare le informazioni di ripristino in Active Directory Domain Services. Per istruzioni su come configurare Active Directory, vedere [Guida alla configurazione di crittografia unità BitLocker: backup delle informazioni di ripristino di BitLocker e TPM in Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).<br/> |
| <dl> <dt>**Connessione non riuscita**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | Non è possibile salvare le informazioni di ripristino nella rete. Il computer è stato configurato per archiviare le informazioni di ripristino in Active Directory Domain Services. Per continuare, è necessaria una connessione di rete.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

Il metodo **ChangeOwnerAuth** esegue il backup della nuova autorizzazione del proprietario del TPM per Active Directory Domain Services se sono state configurate le impostazioni criteri di gruppo appropriate.

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

 

 
