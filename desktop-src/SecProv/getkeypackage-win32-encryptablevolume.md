---
description: Esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non sono presenti file di backup dei dati.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Metodo GetKeyPackage della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316108"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyPackage della \_ classe EncryptableVolume Win32

Il metodo **GetKeyPackage** della classe [**\_ EncryptableVolume di Win32**](win32-encryptablevolume.md) Esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non sono presenti file di backup dei dati.

Le informazioni esportate sono costituite dalla chiave di crittografia del volume protetta da una protezione con chiave di tipo "Numerical password" o "External Key". Per utilizzare questo pacchetto, è necessario salvare anche la password numerica o la chiave esterna corrispondente.

> [!IMPORTANT]
> Se si sceglie di esportare un pacchetto di chiavi, assicurarsi di conservarle in una posizione ben protetta. Non includere queste informazioni nel computer. Se il pacchetto di chiavi viene smarrito o rubato, sarà necessario decrittografare il volume e ricrittografarlo utilizzando una nuova chiave.

 

In caso di errore di un'unità, lo strumento di ripristino di BitLocker esiste per facilitare il recupero dei dati disponibili. Per ulteriori informazioni sul modo in cui questo strumento può utilizzare il pacchetto di chiavi, vedere [come utilizzare lo strumento di ripristino di BitLocker per ripristinare i dati da un volume crittografato in Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata. Per esportare un pacchetto di chiavi, è necessario usare una protezione con chiave di tipo "Numerical password" o "External Key".

</dd> <dt>

*Pacchetto di \[ \] pacchetti* in \[ uscita\]
</dt> <dd>

Tipo: **Uint8**

Flusso di byte che contiene la chiave di crittografia per un volume, protetto dalla protezione con chiave specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key". Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.<br/> |



 

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

 

 
