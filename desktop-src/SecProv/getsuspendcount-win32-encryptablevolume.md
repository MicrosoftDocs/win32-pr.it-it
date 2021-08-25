---
description: Recupera il numero di volte in cui BitLocker è stato sospeso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Metodo GetSuspendCount della classe Win32_EncryptableVolume (Activdbg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 468bd6cdc8f3df7efba26997fd76b0724d3e4cc5da552275dad5201adc469f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906351"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Metodo GetSuspendCount della classe \_ EncryptableVolume Win32

Il **metodo GetSuspendCount** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera il numero di riavvii prima che la protezione venga ripresa automaticamente.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SuspendCount* 
</dt> <dd>

Valore intero compreso tra 0 e 15.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice restituito                                                                                          | Descrizione                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Il metodo è stato eseguito correttamente.<br/>                                      |
| <dl> <dt>**ERRORE \_ NON \_ SUPPORTATO**</dt> </dl> | Restituito se il volume non è sospeso o non è un volume del sistema operativo.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si applica solo al volume del sistema operativo e solo se viene effettivamente sospeso al momento. Se il volume non è sospeso o non è un volume del sistema operativo, **verrà restituito ERROR \_ NOT \_ SUPPORTED.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 Enterprise, Windows 8 Pro solo app \[ desktop\]<br/>                                    |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>Activdbg.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




