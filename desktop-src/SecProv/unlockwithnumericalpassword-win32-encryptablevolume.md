---
description: Usa una password numerica fornita per accedere al contenuto di un volume di dati.
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
ms.openlocfilehash: d52cd0dd2c80bf00a55bef0fde40008f7133f28cb3be0a9aa5366076c6502b9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891295"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithNumericalPassword della classe \_ EncryptableVolume Win32

Il **metodo UnlockWithNumericalPassword** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa una password numerica fornita per accedere al contenuto di un volume di dati.

Per poter sbloccare il volume con questo metodo, la chiave di crittografia del volume deve essere protetta con una o più chiavi protette di tipo "Password numerica" (usando il metodo [**ProtectKeyWithNumericalPassword).**](protectkeywithnumericalpassword-win32-encryptablevolume.md)

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumericalPassword* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la password numerica.

La password numerica deve contenere 48 cifre. Queste cifre possono essere suddivise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 65536. Supponendo che un gruppo di sei cifre sia etichettato come x1, x2, x3, x4, x5 e x6, la cifra checksum x6 viene calcolata come –x1+x2–x3+x4-x5 mod 11.

I gruppi di cifre possono facoltativamente essere separati da uno spazio o un trattino. Pertanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere password numeriche valide.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                             | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>            | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt> </dl>     | Il volume non dispone di una protezione con chiave di tipo "Password numerica".<br/> Il *formato del parametro NumericalPassword* è valido, ma non è possibile usare una password numerica per sbloccare il volume.<br/>           |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>    | Il *parametro NumericalPassword* non è in grado di sbloccare il volume.<br/> Esistono una o più chiavi di protezione di tipo "Password numerica", ma il parametro *NumericalPassword* specificato non è in grado di sbloccare il volume.<br/> |
| <dl> <dt>**FVE \_ E \_ FORMATO \_ PASSWORD \_ NON**</dt> <dt>2150694965 (0x80310035)</dt> </dl> | Il *formato del parametro NumericalPassword* non è valido.<br/>                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
