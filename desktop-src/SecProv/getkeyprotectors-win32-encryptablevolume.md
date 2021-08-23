---
description: Elenca le protezione usate per proteggere la chiave di crittografia del volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Metodo GetKeyProtectors della Win32_EncryptableVolume classe
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
ms.openlocfilehash: 01342b932e3a285870026ef57bfa0040d1659ca7af1165e6fb67f3af780896d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667681"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectors della classe \_ EncryptableVolume Win32

Il **metodo GetKeyProtectors** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) elenca le protezione usate per proteggere la chiave di crittografia del volume. Se viene specificato un tipo di protezione, vengono restituite solo le protezione con chiave del volume del tipo specificato.

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

Tipo: **uint32**

Intero senza segno che specifica il tipo di protezione con chiave da restituire.

Se questo parametro non viene specificato, vengono restituite tutte le protezione con chiave disponibili del volume.



| Valore                                                                         | Significato                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Tutti i tipi.<br/> Vengono restituite tutte le protezione con chiave.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Chiave esterna.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Password numerica.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM e PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM e chiave di avvio.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM e PIN e chiave di avvio.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Chiave pubblica.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Passphrase.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificato TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | ID di sicurezza (SID)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] string**

Matrice di stringhe che identificano le protezione con chiave usate per proteggere la chiave di crittografia del volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro VolumeKeyProtectorID* è specificato ma non fa riferimento a un *keyProtectorType valido.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                   |



 

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

 

 
