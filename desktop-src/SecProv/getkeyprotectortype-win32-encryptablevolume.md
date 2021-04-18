---
description: Indica il tipo di una protezione con chiave specificata.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Metodo GetKeyProtectorType della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529785"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorType della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectorType** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica il tipo di una protezione con chiave specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*KeyProtectorType* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Unsigned Integer che specifica il tipo della protezione con chiave.



| Valore                                                                         | Significato                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tipo di protezione sconosciuto o altro<br/>           |
| <dl> <dt>1</dt> </dl>  | TPM (Trusted Platform Module)<br/>             |
| <dl> <dt>2</dt> </dl>  | Chiave esterna<br/>                              |
| <dl> <dt>3</dt> </dl>  | Password numerica<br/>                        |
| <dl> <dt>4</dt> </dl>  | TPM e PIN<br/>                               |
| <dl> <dt>5</dt> </dl>  | TPM e chiave di avvio<br/>                       |
| <dl> <dt>6</dt> </dl>  | TPM, PIN e chiave di avvio<br/>               |
| <dl> <dt>7</dt> </dl>  | Chiave pubblica<br/>                                |
| <dl> <dt>8</dt> </dl>  | Passphrase<br/>                                |
| <dl> <dt>9</dt> </dl>  | Certificato TPM<br/>                           |
| <dl> <dt>10</dt> </dl> | Protezione CNG (CryptoAPI Next Generation)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il parametro *VolumeKeyProtectorID* non fa riferimento a un *KeyProtectorType* valido.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>  |



 

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

 

 
