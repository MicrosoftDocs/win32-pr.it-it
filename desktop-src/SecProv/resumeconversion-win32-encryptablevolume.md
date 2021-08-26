---
description: Riprende la crittografia o la decrittografia di un volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Metodo ResumeConversion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e1b3908f77b72f7f9a5ca0583193784ba054a50ab59aa63dad1c13b9f03317e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992671"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Metodo ResumeConversion della classe \_ EncryptableVolume Win32

Il **metodo ResumeConversion** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) riprende la crittografia o la decrittografia di un volume.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione può riprendere solo un'operazione di pulizia. Per altre informazioni, vedere [**PauseConversion.**](pauseconversion-win32-encryptablevolume.md)

 

## <a name="syntax"></a>Sintassi


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se questo metodo viene usato in un volume completamente crittografato o completamente decrittografato o se la crittografia/decrittografia è già in corso nel volume, viene restituito 0 presupponendo che non si verifichino altri errori.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/> |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl> | Il volume è bloccato.<br/>      |



 

## <a name="remarks"></a>Commenti

Se questo metodo viene usato in un volume con crittografia/decrittografia sospesa, l'esecuzione corretta di questo metodo fa sì che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che è in corso la crittografia o la decrittografia.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
