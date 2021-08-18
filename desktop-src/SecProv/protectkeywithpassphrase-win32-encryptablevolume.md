---
description: 'Metodo ProtectKeyWithPassphrase della Win32_EncryptableVolume: usa la passphrase per ottenere la chiave derivata.'
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
ms.openlocfilehash: c0d87eb21ea505b13ce3aacfe8be6ff1fa9d266ba2a781d6b8e6fc4d77dac10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004359"
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
| <dl> <dt>**FVE \_ E \_ NON CONSENTITO IN MODALITÀ \_ \_ \_ \_ PROVVISORIA**</dt> 2150694976 <dt>(0x80310040)</dt> </dl>         | Crittografia unità BitLocker può essere usato solo a scopo di ripristino quando viene usato in Cassaforte predefinita.<br/>                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ NOT ALLOWED \_ 2150695018**</dt> <dt>(0x8031006A)</dt> </dl>     | Criteri di gruppo non consente la creazione di una passphrase.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ FIPS \_ IMPEDISCE \_ L'2150695020 PASSPHRASE**</dt> <dt>(0x8031006C)</dt> </dl>           | L'impostazione di Criteri di gruppo che richiede la conformità FIPS ha impedito la generazione o l'uso della passphrase.<br/> |
| <dl> <dt>**FVE \_ E \_ CRITERIO \_ LUNGHEZZA \_ PASSPHRASE \_**</dt> NON VALIDA 2150695040 <dt>(0x80310080)</dt> </dl>  | La passphrase specificata non soddisfa i requisiti di lunghezza minima o massima.<br/>                             |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PASSPHRASE \_ TOO \_ SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt> </dl>      | La passphrase non soddisfa i requisiti di complessità impostati dall'amministratore in Criteri di gruppo.<br/>            |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl>                       | Il volume è già bloccato da Crittografia unità BitLocker. È necessario sbloccare l'unità Pannello di controllo.<br/>     |
| <dl> <dt>**FVE \_ E \_ OVERLAPPED \_ UPDATE 2150694948**</dt> <dt>(0x80310024)</dt> </dl>                   | Il blocco di controllo per il volume crittografato è stato aggiornato da un altro thread.<br/>                                     |
| <dl> <dt>**FVE \_ E \_ PROTEZIONE CON CHIAVE NON \_ \_ \_ SUPPORTATA**</dt> <dt>2150695017 (0x80310069)</dt> </dl>       | La protezione con chiave non è supportata dalla versione di Crittografia unità BitLocker attualmente nel volume.<br/>      |
| <dl> <dt>**FVE \_ PASSPHRASE DEL VOLUME DEL SISTEMA \_ \_ OPERATIVO NON \_ \_ \_ CONSENTITA**</dt> 2150695021 <dt>(0x8031006D)</dt> </dl> | Non è possibile aggiungere la passphrase al volume del sistema operativo. <br/>                                               |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS 2150694960**</dt> <dt>(0x80310030)</dt> </dl>                    | La protezione con chiave specificata esiste già in questo volume.<br/>                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows solo app desktop Ultimate 7 \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




