---
description: Crea un volume BitLocker con il tipo di file system specificato del volume di individuazione.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Metodo PrepareVolume della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 67b36703883825d4144037c54ffb55c00308ed1cfb8ee3e4b074d75d63bf7390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891547"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Metodo PrepareVolume della classe \_ EncryptableVolume Win32

Il **metodo PrepareVolume** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) crea un volume BitLocker con il file system specificato del volume di individuazione. Questo metodo deve essere chiamato prima che il volume possa essere protetto con uno dei **metodi ProtectKeyWith. \***

## <a name="syntax"></a>Sintassi

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*DiscoveryVolumeType* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il tipo di volume di individuazione.

| Valore               | Significato                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;Nessuno&gt;**    | Nessun volume di individuazione. Questo valore crea un volume BitLocker nativo. |
| **&lt;Predefinito&gt;** | Questo valore è il comportamento predefinito.                                |
| **FAT32**           | Questo valore crea un volume di individuazione FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Intero che specifica il tipo di crittografia. Può essere uno dei valori seguenti.

| Valore                                                                                                                                                                                                                                       | Significato                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Non specificato**</dt> <dt>0</dt> </dl> | Il tipo di crittografia non è specificato.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Crittografia software.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Crittografia hardware.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

| Codice/valore restituito      | Descrizione                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | Il metodo è stato eseguito correttamente.<br/> |

## <a name="remarks"></a>Commenti

Se non si chiama questo metodo quando si abilita un volume BitLocker, è uguale a chiamare questo metodo con il valore predefinito nel *parametro DiscoveryVolumeType.*

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows 7 app desktop Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
