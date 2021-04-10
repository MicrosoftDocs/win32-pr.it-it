---
description: Protegge la chiave di crittografia del volume con una password a 48 cifre formattata in modo specifico.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Metodo ProtectKeyWithNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883597"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithNumericalPassword della \_ classe EncryptableVolume Win32

Il metodo **ProtectKeyWithNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume con una password a 48 cifre formattata in modo specifico. Questa password numerica può essere utilizzata per il recupero dagli errori di autenticazione di altre protezioni con chiave (ad esempio, TPM).

Viene creata una protezione con chiave di tipo "password numerica" per il volume.

Usare il metodo [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) per convalidare il formato della password numerica.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica un identificatore assegnato dall'utente per la protezione con chiave. Se questo parametro non è specificato, viene utilizzato un valore blank.

</dd> <dt>

*NumericalPassword* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la password numerica 48-digit formattata in modo specifico.

La password numerica deve contenere 48 cifre. Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 720896. Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.

I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino. Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.

Se non viene specificata alcuna password numerica, ne viene generata una in modo casuale. Usare il metodo [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) per ottenere la password generata in modo casuale.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che rappresenta l'identificatore univoco associato alla protezione creata e che può essere utilizzata per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il formato del parametro *NumericalPassword* non è valido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>                                           |
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

 

 
