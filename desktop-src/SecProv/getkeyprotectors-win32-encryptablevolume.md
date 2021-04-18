---
description: Elenca le protezioni utilizzate per proteggere la chiave di crittografia del volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Metodo GetKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306395"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectors della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) elenca le protezioni usate per proteggere la chiave di crittografia del volume. Se viene fornito un tipo di protezione, vengono restituite solo le protezioni con chiave del volume del tipo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*KeyProtectorType* \[ in, facoltativo\]
</dt> <dd>

Tipo: **UInt32**

Unsigned Integer che specifica il tipo di protezione con chiave da restituire.

Se questo parametro non viene specificato, vengono restituite tutte le protezioni con chiave disponibili del volume.



| Valore                                                                         | Significato                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tutti i tipi.<br/> Vengono restituite tutte le protezioni con chiave.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Chiave esterna.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Password numerica.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM e PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM e chiave di avvio.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM, PIN e chiave di avvio.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Chiave pubblica.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificato TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | ID di sicurezza (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa \[ \]**

Matrice di stringhe che identificano le protezioni con chiave utilizzate per proteggere la chiave di crittografia del volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il parametro *VolumeKeyProtectorID* è specificato ma non fa riferimento a un *KeyProtectorType* valido.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                   |



 

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

 

 
