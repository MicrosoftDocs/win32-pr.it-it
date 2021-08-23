---
description: Smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Metodo Lock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5053fe027bbae51ce93feb11de5f95bde1d7b17c85a05df1386e5470b1b20fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867661"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Metodo Lock della classe \_ EncryptableVolume Win32

Il **metodo Lock** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema. Il contenuto del volume rimane inaccessibile fino a quando non viene sbloccato tramite il [**metodo UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**il metodo UnlockWithNumericalPassword.**](unlockwithnumericalpassword-win32-encryptablevolume.md) Questo metodo non può essere eseguito correttamente per il volume del sistema operativo attualmente in esecuzione.

> [!Note]  
> Se il disco supporta la crittografia hardware, la banda viene impostata su "bloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ForceDismount* \[ in, facoltativo\]
</dt> <dd>

Tipo: **booleano**

Se **true,** il disco viene smontato forzatamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                           | Descrizione                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ACCESSO \_ negato**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Le applicazioni accedono a questo volume. Se tutti gli accessi non sono esclusivi, se si specifica il parametro *ForceDismount* come true, il metodo può essere eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | Il volume è completamente decrittografato e non può essere bloccato.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ E \_ PROTEZIONE \_ DISABILITATA**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | La chiave di crittografia del volume è disponibile in chiaro sul disco, impedendo il blocco del volume.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ RECOVERY KEY REQUIRED \_ \_ 2150694946**</dt> <dt>(0x80310022)</dt> </dl> | Il volume non dispone di protezione con chiave di tipo "Password numerica" o "Chiave esterna" necessaria per sbloccare il volume.<br/>                            |



 

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

 

 
