---
description: Usa la passphrase per ottenere la chiave derivata.
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
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317681"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithPassphrase della \_ classe EncryptableVolume Win32

Il metodo **UnlockWithPassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata. Dopo aver calcolato la chiave derivata, viene utilizzata la chiave derivata per sbloccare la chiave master del volume crittografato.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Passphrase* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la passphrase.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                       | Descrizione                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Il metodo è stato eseguito correttamente.<br/>                                                                                     |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                              |
| <dl> <dt>**FVE \_ E \_ FIPS \_ impedisce la \_ passphrase**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>          | L'impostazione di criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'utilizzo della passphrase. <br/> |
| <dl> <dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza passphrase non valida**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.<br/>                              |
| <dl> <dt>**FVE \_ \_Passphrase dei criteri E \_ \_ troppo \_ semplice**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore in criteri di gruppo.<br/>             |
| <dl> <dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt> </dl>              | Il volume non può essere sbloccato con le informazioni fornite. <br/>                                                  |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>               | La protezione con chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




