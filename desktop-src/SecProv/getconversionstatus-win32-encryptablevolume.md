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
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878934"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetConversionStatus della \_ classe EncryptableVolume Win32

Il metodo **GetConversionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica lo stato della crittografia o della decrittografia nel volume.

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

*ConversionStatus* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Stato di crittografia o decrittografia del volume. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <dt>**FullyDecrypted**</dt> <dt>0</dt> </dl>                         | Per un disco rigido standard (HDD), il volume viene completamente decrittografato.<br/> Per un disco rigido crittografato hardware (EHDD), il volume viene costantemente sbloccato.<br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <dt>**FullyEncrypted**</dt> <dt>1</dt> </dl>                         | Per un disco rigido standard (HDD), il volume è completamente crittografato.<br/> Per un disco rigido crittografato hardware (EHDD), il volume non viene sbloccato continuamente.<br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <dt>**EncryptionInProgress**</dt> <dt>2</dt> </dl> | Il volume è parzialmente crittografato.<br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <dt>**DecryptionInProgress**</dt> <dt>3</dt> </dl> | Il volume è parzialmente crittografato.<br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <dt>**EncryptionPaused**</dt> <dt>4</dt> </dl>                 | Il volume è stato sospeso durante lo stato della crittografia. Il volume è parzialmente crittografato.<br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <dt>**DecryptionPaused**</dt> <dt>5</dt> </dl>                 | Il volume è stato sospeso durante lo stato di decrittografia. Il volume è parzialmente crittografato.<br/>                                                                  |



 

</dd> <dt>

*EncryptionPercentage* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Percentuale del volume crittografato. Si tratta di un numero intero compreso tra 0 e 100.

A causa dell'arrotondamento dei numeri, una percentuale di crittografia pari a 0 o 100 non indica necessariamente che il disco è completamente decrittografato o completamente crittografato. Usare sempre *ConversionStatus* per determinare se il disco è effettivamente completamente decrittografato o completamente crittografato.

</dd> <dt>

*EncryptionFlags* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Flag che descrivono il comportamento di crittografia.

Una combinazione di 32 bit con i bit seguenti attualmente definiti.



| Valore                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia. Se la crittografia è stata sospesa o arrestata, la chiamata del metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) riprende effettivamente la conversione e il valore di questo bit viene ignorato. Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, decrittografia nello stato di avanzamento o decrittografia in pausa. Se questo bit è zero, vale a dire che non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Eseguire la cancellazione su richiesta dello spazio disponibile nel volume. La chiamata al metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) con questo set di bit è consentita solo quando il volume non è attualmente in fase di conversione o cancellazione e si trova in uno stato "crittografato".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Eseguire in modo sincrono l'operazione richiesta. La chiamata verrà bloccata fino a quando l'operazione richiesta non è stata completata o è stata interrotta. Questo flag è supportato solo con il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) . Questo flag può essere **specificato quando viene chiamata la crittografia per** riprendere la crittografia arrestata o interrotta o cancellare o quando è in corso la crittografia o la cancellazione. Ciò consente al chiamante di riprendere l'attesa in modo sincrono finché il processo non viene completato o interrotto.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

*WipingStatus* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Stato cancellazione spazio libero. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                               | Significato                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <dt>**FreeSpaceNotWiped**</dt> <dt>0</dt> </dl>                                 | Lo spazio libero non è stato cancellato.<br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <dt>**FreeSpaceWiped**</dt> <dt>1</dt> </dl>                                             | Lo spazio libero è stato cancellato.<br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt> </dl> | La cancellazione dello spazio disponibile è attualmente in corso.<br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt> </dl>                 | Cancellazione dello spazio disponibile sospesa.<br/>          |



 

</dd> <dt>

*WipingPercentage* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Valore compreso tra 0 e 100 che specifica la percentuale di spazio libero che è stata cancellata.

</dd> <dt>

*PrecisionFactor* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Valore compreso tra 0 e 4 che specifica il livello di precisione

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

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

 

 
