---
description: Indica l'algoritmo di crittografia e le dimensioni della chiave usati nel volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Metodo GetEncryptionMethod della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316118"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Metodo GetEncryptionMethod della \_ classe EncryptableVolume Win32

Il metodo **GetEncryptionMethod** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica l'algoritmo di crittografia e le dimensioni della chiave usati nel volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptionMethod* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Unsigned Integer che specifica l'algoritmo di crittografia e le dimensioni della chiave utilizzati nel volume.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Nessuno**</dt> <dt>0</dt> </dl>                                | Il volume non è crittografato.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ con \_ diffusore**</dt> <dt>1</dt> </dl> | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello di diffusione, usando una dimensione della chiave AES di 128 bit. Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versione successiva.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ con \_ diffusore**</dt> <dt>2</dt> </dl> | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello di diffusione, usando una dimensione della chiave AES di 256 bit. Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versione successiva.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 128 bit.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 256 bit.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**Hardware \_ CRITTOGRAFIA**</dt> <dt>5</dt> </dl>         | Il volume è stato completamente o parzialmente crittografato utilizzando le funzionalità hardware dell'unità.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | Il volume è stato completamente o parzialmente crittografato con XTS usando il Advanced Encryption Standard (AES) e una dimensione della chiave AES di 128 bit. Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10, versione 1511 o successiva.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | Il volume è stato completamente o parzialmente crittografato con XTS usando il Advanced Encryption Standard (AES) e una dimensione della chiave AES di 256 bit. Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10, versione 1511 o successiva.<br/>                          |
| <dl> <dt>(UInt32) – 1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> Il volume è stato completamente o parzialmente crittografato con un algoritmo sconosciuto e le dimensioni della chiave.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ out\]
</dt> <dd>

Tipo: **stringa**

L'algoritmo di crittografia viene configurato nell'unità di crittografia automatica. Una stringa null indica che BitLocker utilizza la crittografia software o che non viene segnalato alcun metodo di crittografia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

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

 

 
