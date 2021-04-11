---
description: Crea un volume di BitLocker con il tipo di file system specificato del volume di individuazione.
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
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128750"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a>Metodo PrepareVolume della \_ classe EncryptableVolume Win32

Il metodo **PrepareVolume** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) crea un volume di BitLocker con il tipo di file system specificato del volume di individuazione. Questo metodo deve essere chiamato prima che il volume possa essere protetto con uno qualsiasi dei metodi **ProtectKeyWith \** _.

## <a name="syntax"></a>Sintassi

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

_DiscoveryVolumeType * \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il tipo di volume di individuazione.

| Valore               | Significato                                                            |
|---------------------|--------------------------------------------------------------------|
| **&lt;nessuno&gt;**    | Nessun volume di individuazione. Questo valore consente di creare un volume nativo di BitLocker. |
| **&lt;predefinita&gt;** | Questo valore è il comportamento predefinito.                                |
| **FAT32**           | Questo valore consente di creare un volume di individuazione FAT32.                       |

</dd> <dt>

*ForceEncryptionType* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Integer che specifica il tipo di crittografia. Può corrispondere a uno dei valori seguenti.

| Valore                                                                                                                                                                                                                                       | Significato                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> Non <dt>**specificato**</dt> <dt>0</dt> </dl> | Il tipo di crittografia non è specificato.<br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <dt>**Software**</dt> <dt>1</dt> </dl>             | Crittografia software.<br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <dt>**Hardware**</dt> <dt>2</dt> </dl>             | Crittografia hardware.<br/>                  |

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

| Codice/valore restituito      | Descrizione                     |
|------------------------|---------------------------------|
| **S_OK** <br/> 0 (0x0) | Il metodo è stato eseguito correttamente.<br/> |

## <a name="remarks"></a>Commenti

Se questo metodo non viene chiamato quando si Abilita un volume di BitLocker, equivale a chiamare questo metodo con il valore predefinito nel parametro *DiscoveryVolumeType* .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
