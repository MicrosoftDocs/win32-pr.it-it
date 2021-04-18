---
description: Elimina tutte le protezioni con chiave per il volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Metodo DeleteKeyProtectors della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312765"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo DeleteKeyProtectors della \_ classe EncryptableVolume Win32

Il metodo **DeleteKeyProtectors** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) Elimina tutte le protezioni con chiave per il volume.

Se un volume non crittografato dispone di protezioni con chiave, quando **DeleteKeyProtectors** viene eseguito correttamente, il volume ripristina un file system NTFS standard.

Se il volume non è ancora completamente decrittografato, usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di eseguire **DeleteKeyProtectors** per assicurarsi che le parti crittografate del volume rimangano accessibili.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ \_Chiave E \_ obbligatoria**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | Non è possibile rimuovere l'ultima protezione con chiave per un volume parzialmente o completamente crittografato se sono abilitate le protezioni con chiave. Usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di rimuovere l'ultima protezione con chiave per assicurarsi che le parti crittografate del volume rimangano accessibili. <br/> |
| <dl> <dt>**FVE \_ E \_ \_ con binding VOLUME \_ già**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Non è possibile eliminare le protezioni con chiave perché uno di essi è usato per sbloccare automaticamente il volume. <br/> Usare [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per disabilitare lo sblocco automatico prima di eseguire questo metodo.<br/>                                                       |



 

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

 

 
