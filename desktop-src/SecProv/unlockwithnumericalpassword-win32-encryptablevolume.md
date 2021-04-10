---
description: Usa una password numerica specificata per accedere al contenuto di un volume di dati.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Metodo UnlockWithNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878918"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithNumericalPassword della \_ classe EncryptableVolume Win32

Il metodo **UnlockWithNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa una password numerica specificata per accedere al contenuto di un volume di dati.

La chiave di crittografia del volume deve essere stata protetta con una o più protezioni con chiave di tipo "password numerica" (usando il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) per poter sbloccare il volume con questo metodo.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumericalPassword* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la password numerica.

La password numerica deve contenere 48 cifre. Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 65536. Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.

I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino. Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | Il volume non dispone di una protezione con chiave di tipo "password numerica".<br/> Il formato del parametro *NumericalPassword* è valido, ma non è possibile usare una password numerica per sbloccare il volume.<br/>           |
| <dl> <dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | Il parametro *NumericalPassword* non è in grado di sbloccare il volume.<br/> Sono presenti una o più protezioni con chiave di tipo "password numerica", ma il parametro *NumericalPassword* specificato non è in grado di sbloccare il volume.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ \_ formato della PASSWORD non valido**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | Il formato del parametro *NumericalPassword* non è valido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/>                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
