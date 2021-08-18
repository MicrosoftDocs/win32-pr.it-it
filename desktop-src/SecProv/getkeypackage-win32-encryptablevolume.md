---
description: Esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non esistono file di backup dei dati.
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
ms.openlocfilehash: 777c68bab142fc0f27d9200d2aea1ff0c45c47181d951600dcc96bb0e623b6ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892358"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyPackage della classe \_ EncryptableVolume Win32

Il **metodo GetKeyPackage** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) esporta informazioni che possono aiutare a recuperare i dati crittografati quando l'unità è gravemente danneggiata e non sono presenti file di backup dei dati.

Le informazioni esportate sono costituite dalla chiave di crittografia del volume protetta da una protezione con chiave di tipo "Password numerica" o "Chiave esterna". Per usare questo pacchetto, è necessario salvare anche la password numerica o la chiave esterna corrispondente.

> [!IMPORTANT]
> Se si sceglie di esportare un pacchetto di chiavi, assicurarsi di mantenere queste informazioni in un percorso protetto. Non portare queste informazioni con il computer. Se questo pacchetto di chiavi viene smarrito o rubato, sarà necessario decrittografare il volume e ricrittografarlo usando una nuova chiave.

 

In caso di errore dell'unità, lo strumento di ripristino BitLocker è disponibile per recuperare i dati disponibili. Per altre informazioni su come questo strumento può usare il pacchetto di chiavi, vedere How [to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco usato per gestire una protezione con chiave di volume crittografata. Per esportare un pacchetto di chiavi, è necessario usare una protezione con chiave di tipo "Password numerica" o "Chiave esterna".

</dd> <dt>

*KeyPackage \[ \]* \[out\]
</dt> <dd>

Tipo: **uint8**

Flusso di byte che contiene la chiave di crittografia per un volume, protetto dalla protezione della chiave specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | La protezione della chiave specificata non esiste nel volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ INVALID \_ PROTECTOR \_ TYPE**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Il *parametro VolumeKeyProtectorID* non fa riferimento a una protezione della chiave di tipo "Numerical Password" o "External Key". Usare il [**metodo ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione della chiave del tipo appropriato.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
