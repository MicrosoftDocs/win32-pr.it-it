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
ms.openlocfilehash: f9f4a2ad20af7c5ee3ba3afd8e2d9e56d0720b38d7afc2b01042e440cc85bf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892449"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a>Metodo GetEncryptionMethod della classe \_ EncryptableVolume Win32

Il **metodo GetEncryptionMethod** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica l'algoritmo di crittografia e le dimensioni della chiave usate nel volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptionMethod* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Intero senza segno che specifica l'algoritmo di crittografia e le dimensioni della chiave utilizzate nel volume.



| Valore                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <dt>**Nessuno**</dt> <dt>0</dt> </dl>                                | Il volume non è crittografato.<br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <dt>**AES \_ 128 \_ CON \_ DIFFUSORE**</dt> <dt>1</dt> </dl> | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello diffusore, usando una dimensione della chiave AES di 128 bit. Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versioni successive.<br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <dt>**AES \_ 256 \_ CON \_ DIFFUSORE**</dt> <dt>2</dt> </dl> | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello diffusore, usando una dimensione della chiave AES di 256 bit. Questo metodo non è più disponibile nei dispositivi che eseguono Windows 8.1 o versioni successive.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                             | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 128 bit.<br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                             | Il volume è stato completamente o parzialmente crittografato con l'algoritmo Advanced Encryption Standard (AES), usando una dimensione della chiave AES di 256 bit.<br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <dt>**HARDWARE \_ CRITTOGRAFIA**</dt> <dt>5</dt> </dl>         | Il volume è stato crittografato completamente o parzialmente usando le funzionalità hardware dell'unità.<br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt> </dl>                                | Il volume è stato completamente o parzialmente crittografato con XTS usando Advanced Encryption Standard (AES) e una dimensione della chiave AES di 128 bit. Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10 versione 1511 o successiva.<br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt> </dl>                                | Il volume è stato completamente o parzialmente crittografato con XTS usando Advanced Encryption Standard (AES) e una dimensione della chiave AES di 256 bit. Questo metodo è disponibile solo nei dispositivi che eseguono Windows 10 versione 1511 o successiva.<br/>                          |
| <dl> <dt>(uint32)-1</dt> </dl>                                                                                                                                                          | UNKNOWN<br/> Il volume è stato crittografato completamente o parzialmente con un algoritmo sconosciuto e le dimensioni della chiave.<br/>                                                                                                                                            |



 

</dd> <dt>

*SelfEncryptionDriveEncryptionMethod* \[ Cambio\]
</dt> <dd>

Tipo: **stringa**

L'algoritmo di crittografia è configurato nell'unità autocrittografa. Una stringa Null indica che BitLocker usa la crittografia software o non viene segnalato alcun metodo di crittografia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

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

 

 
