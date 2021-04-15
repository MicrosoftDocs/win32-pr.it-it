---
description: Modifica il PIN associato a un volume crittografato.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Metodo Changepin aggiorna della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525693"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a>Metodo Changepin aggiorna della \_ classe EncryptableVolume Win32

Il metodo **changepin Aggiorna** della classe [**\_ ENCRYPTABLEVOLUME Win32**](win32-encryptablevolume.md) modifica il PIN associato a un volume crittografato. Se è abilitato il criterio di gruppo "Consenti PIN avanzati per l'avvio", un PIN può contenere lettere, simboli e spazi, oltre ai numeri.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*NewPIN* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa di identificazione personale specificata dall'utente. Questa stringa deve essere composta da una sequenza da 4 a 20 cifre oppure, se è abilitato il criterio di gruppo "Consenti PIN avanzati per l'avvio", da 4 a 20 lettere, simboli, spazi o numeri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Nel computer è presente un CD/DVD di avvio. Rimuovere il CD/DVD e riavviare il computer.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ caratteri PIN non validi**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | Il parametro *NewPIN* contiene caratteri non validi. Quando il Criteri di gruppo "Consenti PIN avanzati per l'avvio" è disabilitato, sono supportati solo i numeri.<br/>                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>     | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key". Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>               | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza PIN non valida**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | Il parametro *NewPIN* specificato può essere composto da più di 20 caratteri, più corto di 4 caratteri o più breve della lunghezza minima specificata da criteri di gruppo.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>        | La protezione con chiave specificata non esiste nel volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Nel computer non sono stati trovati Trusted Platform Module compatibili (TPM).<br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Il metodo **changepin Aggiorna** crea una nuova protezione con TPM e pin in base alle informazioni di protezione esistenti e al pin appena fornito. La nuova protezione avrà lo stesso GUID. Il metodo **changepin Aggiorna** può essere chiamato anche per modificare il pin di una protezione con chiave che usa un PIN, ad esempio TPM e PIN o TPM con pin e USB.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
