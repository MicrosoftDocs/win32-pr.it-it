---
description: Sospende la crittografia o la decrittografia di un volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Metodo PauseConversion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315340"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Metodo PauseConversion della \_ classe EncryptableVolume Win32

Il metodo **PauseConversion** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) sospende la crittografia o la decrittografia di un volume.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione può sospendere un'operazione di cancellazione ma non può sospendere la crittografia basata su hardware.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se questo metodo viene utilizzato in un volume completamente crittografato o completamente decrittografato o se la crittografia/decrittografia è già sospesa nel volume, viene restituito 0 presumendo che non si verifichino altri errori.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="remarks"></a>Commenti

Se questo metodo viene utilizzato in un volume con crittografia/decrittografia in corso, l'esecuzione di questo metodo fa in modo che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la crittografia o la decrittografia è sospesa.

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

 

 
