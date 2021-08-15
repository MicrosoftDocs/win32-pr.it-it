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
ms.openlocfilehash: caa213dbebc7db07851bc8df41b5d9379d3dfe97ee207f9b2578b0567fd9b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892017"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetLockStatus della classe \_ EncryptableVolume Win32

Il **metodo GetLockStatus** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se il contenuto del volume è accessibile da Windows.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LockStatus* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Specifica se il contenuto del volume è accessibile da Windows.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Sbloccato**</dt> <dt>0</dt> </dl> | Per un HDD standard:<br/> Il contenuto completo del volume è accessibile. Un volume sbloccato è completamente decrittografato o ha la chiave di crittografia disponibile nella cancellazione su disco. Il volume contenente il sistema operativo in esecuzione corrente, ad esempio il volume in Windows in esecuzione, è sempre accessibile e non può essere bloccato.<br/> Per un EHDD:<br/> La banda viene sbloccata per sempre.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Bloccato**</dt> <dt>1</dt> </dl>         | Per un HDD standard:<br/> Tutto o una parte del contenuto del volume non sono accessibili. Un volume bloccato deve essere parzialmente o completamente crittografato e non deve avere la chiave di crittografia disponibile nella cancellazione su disco.<br/> Per un EHDD:<br/> La banda è sbloccata o bloccata.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Usare [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) e [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per ottenere l'accesso al contenuto del volume. Usare il [**metodo Lock**](lock-win32-encryptablevolume.md) per rinunciare all'accesso al contenuto del volume.

Il volume che contiene il sistema operativo attualmente in esecuzione è sempre accessibile e non può essere bloccato.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
