---
description: Usa la passphrase per ottenere la chiave derivata.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Metodo ProtectKeyWithPassphrase della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f97806652d86b104a0f333d40d299cfa9502cf3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306379"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithPassphrase della \_ classe EncryptableVolume Win32

Il metodo **ProtectKeyWithPassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata. Dopo che la chiave derivata è stata calcolata, la chiave derivata viene utilizzata per proteggere la chiave master del volume crittografato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica un identificatore di stringa assegnato dall'utente per la protezione con chiave. Se questo parametro non è specificato, viene utilizzato un valore blank.

</dd> <dt>

*Passphrase* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la passphrase.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica in modo univoco la protezione con chiave creata.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                        | Descrizione                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Il metodo è stato eseguito correttamente.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ non \_ consentito \_ in \_ \_ modalità provvisoria**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Crittografia unità BitLocker può essere utilizzato solo per scopi di ripristino se utilizzato in modalità provvisoria.<br/>                     |
| <dl> <dt>**FVE \_ \_Passphrase dei criteri E \_ \_ non \_ consentita**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | Criteri di gruppo non consente la creazione di una passphrase.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ impedisce la \_ passphrase**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | L'impostazione di criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'utilizzo della passphrase.<br/> |
| <dl> <dt>**FVE \_ \_Criterio E \_ \_ \_ lunghezza passphrase non valida**</dt> <dt>2150695040 (0x80310080)</dt> </dl>  | La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.<br/>                             |
| <dl> <dt>**FVE \_ \_Passphrase dei criteri E \_ \_ troppo \_ semplice**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore in criteri di gruppo.<br/>            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Il volume è già bloccato dal Crittografia unità BitLocker. È necessario sbloccare l'unità dal pannello di controllo.<br/>     |
| <dl> <dt>**FVE \_ E \_ \_ aggiornamento 2150694948 sovrapposto**</dt> <dt>(0x80310024)</dt> </dl>                   | Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.<br/>                                     |
| <dl> <dt>**FVE \_ \_Protezione con chiave E \_ \_ non \_ supportata**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | La protezione con chiave non è supportata dalla versione di Crittografia unità BitLocker attualmente nel volume.<br/>      |
| <dl> <dt>**FVE \_ E la \_ passphrase del volume del sistema operativo \_ non è \_ \_ \_ consentita**</dt> <dt>2150695021 (0x8031006D)</dt> </dl> | Non è possibile aggiungere la passphrase al volume del sistema operativo. <br/>                                               |
| <dl> <dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | La protezione con chiave specificata esiste già nel volume.<br/>                                                     |



 

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

 

 




