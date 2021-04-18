---
description: Disabilita o sospende tutte le protezioni con chiave associate a questo volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Metodo DisableKeyProtectors della classe Win32_EncryptableVolume
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
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312764"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo DisableKeyProtectors della \_ classe EncryptableVolume Win32

Il metodo **DisableKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Disabilita o sospende tutte le protezioni con chiave associate a questo volume.

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

Tipo: **UInt32**

Integer che specifica il numero di riavvii per i quali verranno disabilitate le protezioni con chiave. Questo parametro è disponibile solo nei volumi del sistema operativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Questo metodo espone la chiave di crittografia del volume in chiaro sul disco rigido, disattivando la protezione del volume. È consigliabile evitare di usare password o chiavi di crittografia in testo non crittografato.

## <a name="remarks"></a>Commenti

È possibile aggiungere nuove protezioni con chiave anche quando le protezioni con chiave sono disabilitate o sospese. Queste protezioni con chiave rimarranno disabilitate a meno che non venga chiamato [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) .

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> <dt>

[**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
