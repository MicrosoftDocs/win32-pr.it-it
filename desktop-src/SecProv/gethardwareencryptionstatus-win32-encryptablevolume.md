---
description: Determina se il volume si trova in un'unità che supporta o può supportare la crittografia hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Metodo GetHardwareEncryptionStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306398"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetHardwareEncryptionStatus della \_ classe EncryptableVolume Win32

Il metodo **GetHardwareEncryptionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) determina se il volume si trova in un'unità che supporta o può supportare la crittografia hardware.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HardwareEncryptionStatus* \[ out\]
</dt> <dd>

Specifica se l'unità può supportare la crittografia hardware. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                               | Significato                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Non supportato**</dt> <dt>0</dt> </dl> | La crittografia hardware non è supportata.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Nessuna protezione**</dt> <dt>1</dt> </dl> | La crittografia dell'unità non è supportata.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Usa software**</dt> <dt>2</dt> </dl> | Il metodo di crittografia è basato su software.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Usa l'hardware**</dt> <dt>3</dt> </dl> | L'unità supporta la crittografia hardware.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce zero (0) se il volume è compatibile con la crittografia hardware BitLocker. In caso contrario, la funzione restituisce un errore.



| Codice/valore restituito                                                                                                                                 | Descrizione                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il volume è compatibile con la crittografia hardware di BitLocker.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




