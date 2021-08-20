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
ms.openlocfilehash: 7612f7f587d13bb1dbe5fc96d29117d126b3a7166e0172abe98a0777d815effa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004449"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Metodo PauseConversion della classe \_ EncryptableVolume Win32

Il **metodo PauseConversion** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sospende la crittografia o la decrittografia di un volume.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione può sospendere un'operazione di pulizia, ma non può sospendere la crittografia basata su hardware.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.

Se questo metodo viene usato in un volume completamente crittografato o completamente decrittografato o se la crittografia/decrittografia è già sospesa nel volume, viene restituito 0 presupponendo che non si verifichino altri errori.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="remarks"></a>Commenti

Se questo metodo viene usato in un volume con crittografia/decrittografia in corso, la corretta esecuzione di questo metodo fa sì che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la crittografia o la decrittografia è sospesa.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
