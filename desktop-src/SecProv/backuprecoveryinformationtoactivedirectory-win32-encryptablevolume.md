---
description: Backup dei dati di ripristino in Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Metodo BackupRecoveryInformationToActiveDirectory della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bd24a13b7f41f2e87f48c2e5ba97a890d10df3245fcbc6e16f9291c1e0629d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892959"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Metodo BackupRecoveryInformationToActiveDirectory della classe \_ EncryptableVolume Win32

Il **metodo BackupRecoveryInformationToActiveDirectory** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) esegue il backup dei dati di ripristino in Active Directory. Questo metodo richiede che nel volume sia presente una protezione con password numerica. Criteri di gruppo deve essere configurato anche per abilitare il backup delle informazioni di ripristino in Active Directory.

## <a name="syntax"></a>Sintassi


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco usato per gestire una protezione con chiave del volume crittografata. Questa protezione con chiave deve essere una protezione con password numerica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                                         | Criteri di gruppo non consente l'archiviazione delle informazioni di ripristino in Active Directory.<br/>                         |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                             |
| <dl> <dt>**FVE \_ E \_ TIPO DI PROTEZIONE \_ \_ 2150694970**</dt> <dt>NON VALIDO (0x8031003A)</dt> </dl> | La protezione con chiave specificata non è una protezione con chiave numerica. È necessario immettere una protezione con password numerica. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows solo app desktop Ultimate 7 \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




