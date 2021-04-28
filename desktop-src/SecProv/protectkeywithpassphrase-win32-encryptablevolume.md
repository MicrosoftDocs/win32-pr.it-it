---
description: 'Metodo ProtectKeyWithPassphrase della classe Win32_EncryptableVolume : usa la passphrase per ottenere la chiave derivata.'
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Metodo ProtectKeyWithPassphrase della Win32_EncryptableVolume classe
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
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098349"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithPassphrase della classe \_ EncryptableVolume Win32

Il **metodo ProtectKeyWithPassphrase** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa la passphrase per ottenere la chiave derivata. Dopo aver calcolato la chiave derivata, la chiave derivata viene usata per proteggere la chiave master del volume crittografato.

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

Tipo: **string**

Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione con chiave. Se questo parametro non viene specificato, viene usato un valore vuoto.

</dd> <dt>

*Passphrase* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa che specifica la passphrase.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Stringa che identifica in modo univoco la protezione con chiave creata.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                        | Descrizione                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                        | Il metodo è stato eseguito correttamente.<br/>                                                                                    |
| <dl> <dt>**FVE \_ E \_ NON CONSENTITO IN MODALITÀ \_ \_ \_ \_ PROVVISORIA**</dt> <dt>2150694976 (0x80310040)</dt> </dl>         | Crittografia unità BitLocker può essere usato solo a scopo di ripristino quando viene usato in modalità provvisoria.<br/>                     |
| <dl> <dt>**FVE \_ \_ \_ PASSPHRASE DEI CRITERI E NON \_ \_ CONSENTITA**</dt> <dt>2150695018 (0x8031006A)</dt> </dl>     | Criteri di gruppo non consente la creazione di una passphrase.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ IMPEDISCE LA \_ PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt> </dl>           | L'impostazione di Criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'uso della passphrase.<br/> |
| <dl> <dt>**FVE \_ E \_ CRITERIO \_ LUNGHEZZA \_ PASSPHRASE \_**</dt> NON VALIDA <dt>2150695040 (0x80310080)</dt> </dl>  | La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.<br/>                             |
| <dl> <dt>**FVE \_ E \_ \_ PASSPHRASE \_ TROPPO \_ SEMPLICE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore nei criteri di gruppo.<br/>            |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ BLOCCATO**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                       | Il volume è già bloccato da Crittografia unità BitLocker. È necessario sbloccare l'unità Pannello di controllo.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE**</dt> <dt>2150694948 (0x80310024)</dt> </dl>                   | Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.<br/>                                     |
| <dl> <dt>**FVE \_ E \_ KEY \_ PROTECTOR NOT \_ \_ SUPPORTED**</dt> <dt>2150695017 (0X80310069)</dt> </dl>       | La protezione della chiave non è supportata dalla versione di Crittografia unità BitLocker attualmente nel volume.<br/>      |
| <dl> <dt>**FVE \_ \_ \_ \_ PASSPHRASE \_ \_ DEL VOLUME**</dt> DEL SISTEMA OPERATIVO NON CONSENTITA <dt>2150695021 (0x8031006D)</dt> </dl> | La passphrase non può essere aggiunta al volume del sistema operativo. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS**</dt> <dt>2150694960 (0x80310030)</dt> </dl>                    | La protezione della chiave specificata esiste già in questo volume.<br/>                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




