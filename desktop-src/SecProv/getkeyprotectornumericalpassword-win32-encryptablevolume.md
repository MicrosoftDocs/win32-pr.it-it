---
description: Recupera la password numerica per una protezione con chiave specificata.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Metodo GetKeyProtectorNumericalPassword della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306396"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorNumericalPassword della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectorNumericalPassword** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la password numerica per una protezione con chiave specificata del tipo appropriato.

L'identificatore della protezione con chiave deve fare riferimento a una protezione con chiave di tipo "password numerica".

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*NumericalPassword* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che rappresenta la password che può essere utilizzata per sbloccare il volume corrispondente.

La password numerica è 48 cifre. Queste cifre sono divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.

I gruppi di cifre sono separati da un trattino. Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" è il formato della password restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                               |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password".<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                        |



 

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

 

 
