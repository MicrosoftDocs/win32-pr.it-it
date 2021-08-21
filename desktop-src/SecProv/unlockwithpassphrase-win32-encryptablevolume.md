---
description: 'Metodo UnlockWithPassphrase della Win32_EncryptableVolume: usa la passphrase per ottenere la chiave derivata.'
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Metodo UnlockWithPassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7b8a1ef65fd1ca3e279631a1add00ad7c07e2ff870bc24c883fd1877a3800d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004169"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithPassphrase della classe \_ EncryptableVolume Win32

Il **metodo UnlockWithPassphrase** della [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata. Dopo aver calcolato la chiave derivata, la chiave derivata viene usata per sbloccare la chiave master del volume crittografato.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Passphrase* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la passphrase.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.



| Codice/valore restituito                                                                                                                                                                                       | Descrizione                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Il metodo è stato eseguito correttamente.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ IMPEDISCE \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | L'impostazione di Criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'uso della passphrase. <br/> |
| <dl> <dt>**FVE \_ E \_ CRITERI NON VALIDI \_ \_ PASSPHRASE \_ LENGTH**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.<br/>                              |
| <dl> <dt>**FVE \_ \_ \_ PASSPHRASE DEI CRITERI \_ \_ TROPPO**</dt> 2150695041 <dt>(0x80310081)</dt> </dl>     | La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore nei criteri di gruppo.<br/>             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | Il volume non può essere sbloccato con le informazioni fornite. <br/>                                                  |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NOT \_ FOUND**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | La protezione della chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows 7 app desktop Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




