---
description: Recupera il numero di volte in cui BitLocker è stato sospeso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Metodo GetSuspendCount della classe Win32_EncryptableVolume (Activdbg. h)
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
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316101"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Metodo GetSuspendCount della \_ classe EncryptableVolume Win32

Il metodo **GetSuspendCount** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Recupera il numero di riavvii prima che la protezione venga ripresa automaticamente.

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
| <dl> <dt>**\_OK**</dt> </dl>                 | Il metodo è stato eseguito correttamente.<br/>                                      |
| <dl> <dt>**ERRORE \_ non \_ supportato**</dt> </dl> | Restituito se il volume non è sospeso o non è un volume del sistema operativo.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo si applica solo al volume del sistema operativo e solo se è effettivamente sospeso al momento. Se il volume non è sospeso o non è un volume del sistema operativo, verrà restituito l' **errore \_ non \_ supportato** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




