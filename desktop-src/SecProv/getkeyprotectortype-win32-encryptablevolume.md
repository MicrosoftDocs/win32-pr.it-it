---
description: Indica il tipo di una protezione con chiave specificata.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Metodo GetKeyProtectorType della Win32_EncryptableVolume classe
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
ms.openlocfilehash: d55603644c675d80341f1b82713ba66ae9ea310aadc19843dd724b233e34dc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667671"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorType della classe \_ EncryptableVolume Win32

Il **metodo GetKeyProtectorType** della [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica il tipo di protezione con chiave specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco usato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*KeyProtectorType* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Intero senza segno che specifica il tipo della protezione con chiave.



| Valore                                                                         | Significato                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tipo di protezione sconosciuto o di altro tipo<br/>           |
| <dl> <dt>1</dt> </dl>  | TPM (Trusted Platform Module)<br/>             |
| <dl> <dt>2</dt> </dl>  | Chiave esterna<br/>                              |
| <dl> <dt>3</dt> </dl>  | Password numerica<br/>                        |
| <dl> <dt>4</dt> </dl>  | TPM e PIN<br/>                               |
| <dl> <dt>5</dt> </dl>  | TPM e chiave di avvio<br/>                       |
| <dl> <dt>6</dt> </dl>  | TPM e PIN e chiave di avvio<br/>               |
| <dl> <dt>7</dt> </dl>  | Chiave pubblica<br/>                                |
| <dl> <dt>8</dt> </dl>  | Passphrase<br/>                                |
| <dl> <dt>9</dt> </dl>  | Certificato TPM<br/>                           |
| <dl> <dt>10</dt> </dl> | Protezione CryptoAPI Next Generation (CNG)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro VolumeKeyProtectorID* non fa riferimento a un *keyProtectorType valido.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>  |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
