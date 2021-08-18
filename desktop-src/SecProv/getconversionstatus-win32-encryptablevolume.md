---
description: Indica lo stato della crittografia o della decrittografia nel volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Metodo GetConversionStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a93e52e0df7f4ab3fdc4c4686ee05e9c1bc9c2c3082604d922da56bc57cb94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004484"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetConversionStatus della classe \_ EncryptableVolume Win32

Il **metodo GetConversionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica lo stato della crittografia o della decrittografia nel volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato conversione* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Stato di crittografia o decrittografia del volume. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Per un disco rigido standard (HDD), il volume viene decrittografato completamente.<br/> Per un disco rigido crittografato hardware (EHDD), il volume viene sbloccato per sempre.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Per un disco rigido standard (HDD), il volume è completamente crittografato.<br/> Per un disco rigido crittografato hardware (EHDD), il volume non viene sbloccato in modo perpetuo.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | Il volume è parzialmente crittografato.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | Il volume è parzialmente crittografato.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**CrittografiaPausa**</dt> <dt>4</dt> </dl>                 | Il volume è stato sospeso durante l'avanzamento della crittografia. Il volume è parzialmente crittografato.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecrittografiaPausa**</dt> <dt>5</dt> </dl>                 | Il volume è stato sospeso durante l'avanzamento della decrittografia. Il volume è parzialmente crittografato.<br/>                                                                  |



 

</dd> <dt>

*CrittografiaPercentage* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Percentuale del volume crittografato. Intero compreso tra 0 e 100 inclusi.

A causa dell'arrotondamento dei numeri, una percentuale di crittografia di 0 o 100 non indica necessariamente che il disco è completamente decrittografato o completamente crittografato. Usare sempre *ConversionStatus per* determinare se il disco è in realtà completamente decrittografato o completamente crittografato.

</dd> <dt>

*Flag di crittografia* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Flag che descrivono il comportamento di crittografia.

Combinazione di 32 bit con i bit seguenti attualmente definiti.



| Valore                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia. Se la crittografia è stata sospesa o arrestata, la chiamata al metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) riprende in modo efficace la conversione e il valore di questo bit viene ignorato. Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, decrittografia in corso o sospensione della decrittografia. Se questo bit è zero, ovvero non è impostato, all'avvio di un nuovo processo di crittografia verrà eseguita la conversione in modalità completa.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Eseguire la cancellazione su richiesta dello spazio disponibile nel volume. La chiamata [**al metodo Encrypt**](encrypt-win32-encryptablevolume.md) con questo bit impostato è consentita solo quando il volume non è attualmente in fase di conversione o di pulizia e si trova in uno stato "crittografato".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Eseguire l'operazione richiesta in modo sincrono. La chiamata verrà bloccata fino al completamento o all'interruzione dell'operazione richiesta. Questo flag è supportato solo con il [**metodo Encrypt.**](encrypt-win32-encryptablevolume.md) Questo flag può essere specificato quando viene chiamata la funzione **Encrypt** per riprendere la crittografia o la pulizia arrestata o interrotta oppure quando è in corso la crittografia o la pulizia. In questo modo il chiamante può riprendere l'attesa sincrona fino al completamento o all'interruzione del processo.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Stato di pulizia dello spazio disponibile. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | Lo spazio disponibile non è stato cancellato.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | Lo spazio disponibile è stato cancellato.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | La pulizia dello spazio libero è attualmente in corso.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | La pulizia dello spazio disponibile è stata sospesa.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Valore compreso tra 0 e 100 che specifica la percentuale di spazio libero che è stata cancellata.

</dd> <dt>

*PrecisionFactor* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Valore compreso tra 0 e 4 che specifica il livello di precisione

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
