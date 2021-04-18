---
description: Recupera la chiave pubblica e l'identificazione personale del certificato per una protezione con chiave pubblica.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Metodo GetKeyProtectorCertificate della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316107"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorCertificate della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectorCertificate** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la [*chiave pubblica*](../secgloss/p-gly.md) e l'identificazione personale del [*certificato*](../secgloss/c-gly.md) per una protezione con chiave pubblica.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*PublicKey* \[ out\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di byte che specifica la chiave pubblica.

</dd> <dt>

*CertThumbprint* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica l'identificazione digitale del certificato.

</dd> <dt>

*Tipo certificato* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Unsigned Integer che specifica il tipo della protezione con chiave. Questo valore integer viene utilizzato per distinguere tra l'agente recupero dati (DRA) e i certificati utente.



| Valore                                                                        | Significato                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | Il certificato è un DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | Il certificato non è un DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                       | Descrizione                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Il metodo è stato eseguito correttamente.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | La protezione con chiave specificata non è una protezione con chiave. È necessario immettere un'altra protezione con chiave.<br/>            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>                      | Questa unità è bloccata da Crittografia unità BitLocker. È necessario sbloccare questo volume dal pannello di controllo. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ \_Certificato utente del criterio E \_ \_ \_ obbligatorio**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Criteri di gruppo richiede l'utilizzo di un certificato utente, ad esempio una smart card.<br/>                           |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
