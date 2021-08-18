---
description: Disabilita o sospende tutte le protezione con chiave associate a questo volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Metodo DisableKeyProtectors della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 79b9db0043e04d3ab6399677a9e103961d5f1a9b5c5214558bcf53359bedc61a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892540"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo DisableKeyProtectors della classe \_ EncryptableVolume Win32

Il **metodo DisableKeyProtectors** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) disabilita o sospende tutte le protezione con chiave associate a questo volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DisableCount* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint32**

Numero intero che specifica il numero di riavvii per i quali verranno disabilitate le protezione con chiave. Questo parametro è disponibile solo nei volumi del sistema operativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Questo metodo espone la chiave di crittografia del volume in chiaro sul disco rigido, disattivando la protezione del volume. È consigliabile evitare di avere una password o una chiave di crittografia in testo non crittografato.

## <a name="remarks"></a>Commenti

È possibile aggiungere nuove protezione con chiave anche quando le protezione con chiave sono disabilitate o sospese. Queste protezione con chiave rimarranno disabilitate a meno che [**non venga chiamato EnableKeyProtectors.**](enablekeyprotectors-win32-encryptablevolume.md)

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
