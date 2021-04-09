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
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878930"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Metodo Lock della classe Win32 \_ EncryptableVolume

Il metodo **Lock** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema. Il contenuto del volume rimane inaccessibile finché non viene sbloccato tramite il metodo [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o il metodo [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) . Questo metodo non può essere eseguito correttamente per il volume del sistema operativo attualmente in esecuzione.

> [!Note]  
> Se il disco supporta la crittografia hardware, la banda è impostata su "Locked".

 

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

Se **true** , il disco viene smontato forzatamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                           | Descrizione                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ACCESSO \_ negato**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Le applicazioni accedono a questo volume. Se tutti gli accessi non sono esclusivi, l'impostazione del parametro *ForceDismount* su true consente di eseguire correttamente il metodo.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ crittografato**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | Il volume è completamente decrittografato e non può essere bloccato.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ \_Protezione E \_ disabilitata**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | La chiave di crittografia del volume è disponibile in chiaro sul disco, impedendo il blocco del volume.<br/>                                                    |
| <dl> <dt>**FVE \_ \_Chiave di ripristino E \_ \_ richiesta**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | Il volume non dispone di protezioni con chiave di tipo "password numerica" o "chiave esterna" necessarie per sbloccare il volume.<br/>                            |



 

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

 

 
