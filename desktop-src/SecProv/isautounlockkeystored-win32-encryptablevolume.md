---
description: Indica se le chiavi esterne o le informazioni correlate che possono essere utilizzate per sbloccare automaticamente i volumi di dati sono presenti nel volume del sistema operativo attualmente in esecuzione.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Metodo IsAutoUnlockKeyStored della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316094"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Metodo IsAutoUnlockKeyStored della \_ classe EncryptableVolume Win32

Il metodo **IsAutoUnlockKeyStored** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se sono presenti chiavi esterne o informazioni correlate che possono essere usate per sbloccare automaticamente i volumi di dati nel volume del sistema operativo attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsAutoUnlockKeyStored* \[ out\]
</dt> <dd>

Tipo: **booleano**

È **true** se le informazioni che possono essere utilizzate per sbloccare automaticamente i volumi di dati vengono archiviate nel registro di sistema del volume del sistema operativo attualmente in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ \_ volume del sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.<br/>     |



 

## <a name="remarks"></a>Commenti

Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere tutte le informazioni di sblocco dal volume del sistema operativo attualmente in esecuzione.

Le informazioni usate per sbloccare un volume vengono archiviate quando si esegue [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per un volume di dati mentre è in esecuzione il volume del sistema operativo attualmente in esecuzione.

**IsAutoUnlockKeyStored** differisce da [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in quanto, anche se lo sblocco automatico è disabilitato per tutti i volumi di dati attualmente connessi al computer, potrebbero essere ancora presenti informazioni di sblocco associate a volumi di dati o volumi di dati disconnessi che non esistono più.

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

 

 
