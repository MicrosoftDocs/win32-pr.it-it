---
description: Indica se il contenuto del volume è accessibile da Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Metodo GetLockStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306394"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetLockStatus della \_ classe EncryptableVolume Win32

Il metodo **GetLockStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il contenuto del volume è accessibile da Windows.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LockStatus* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Specifica se il contenuto del volume è accessibile da Windows.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Sbloccato**</dt> <dt>0</dt> </dl> | Per un HDD standard:<br/> Il contenuto completo del volume è accessibile. Un volume sbloccato è completamente decrittografato o la chiave di crittografia è disponibile nel disco chiaro su disco. Il volume che contiene il sistema operativo attualmente in esecuzione, ad esempio il volume di Windows in esecuzione, è sempre accessibile e non può essere bloccato.<br/> Per un EHDD:<br/> La banda viene continuamente sbloccata.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Bloccato**</dt> <dt>1</dt> </dl>         | Per un HDD standard:<br/> Tutto o una parte del contenuto del volume non sono accessibili. Un volume bloccato deve essere parzialmente o completamente crittografato e non deve avere la chiave di crittografia disponibile in Clear su disco.<br/> Per un EHDD:<br/> La banda è sbloccata o bloccata.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Usare [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) e [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per ottenere l'accesso al contenuto del volume. Usare il metodo [**Lock**](lock-win32-encryptablevolume.md) per abbandonare l'accesso al contenuto del volume.

Il volume che contiene il sistema operativo attualmente in esecuzione è sempre accessibile e non può essere bloccato.

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

 

 
