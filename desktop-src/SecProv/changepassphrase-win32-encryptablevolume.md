---
description: Usa la nuova passphrase per ottenere una nuova chiave derivata.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Metodo ChangePassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316119"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a>Metodo ChangePassphrase della \_ classe EncryptableVolume Win32

Il metodo **ChangePassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la nuova passphrase per ottenere una nuova chiave derivata. Dopo aver calcolato la chiave derivata, la nuova chiave derivata viene utilizzata per proteggere la chiave master del volume crittografato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*NewPassphrase* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa aggiornata che specifica la passphrase.

</dd> <dt>

*NewProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave del volume crittografata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                       | Descrizione                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Il metodo è stato eseguito correttamente.<br/>                                                                                  |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Il volume è già bloccato dal Crittografia unità BitLocker. È necessario sbloccare l'unità dal pannello di controllo.<br/>   |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                           |
| <dl> <dt>**FVE \_ E \_ \_ aggiornamento 2150694948 sovrapposto**</dt> <dt>(0x80310024)</dt> </dl>                  | Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl>            | La protezione con chiave specificata non è del tipo corretto. <br/>                                                    |
| <dl> <dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza passphrase non valida**</dt> <dt>2150695040 (0x80310080)</dt> </dl> | La passphrase aggiornata specificata non soddisfa i requisiti di lunghezza minima o massima. <br/>                  |
| <dl> <dt>**FVE \_ \_Passphrase dei criteri E \_ \_ troppo \_ semplice**</dt> <dt>2150695041 (0x80310081)</dt> </dl>     | La passphrase aggiornata non soddisfa i requisiti di complessità impostati dall'amministratore in criteri di gruppo. <br/> |



 

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

 

 




