---
description: Elimina tutte le chiavi di protezione per il volume.
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
ms.openlocfilehash: 49884566a45bde4977d56baa3e83ae4c42fdd676447a3da1f3df528ec823c414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004609"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo DeleteKeyProtectors della classe \_ EncryptableVolume Win32

Il **metodo DeleteKeyProtectors** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) elimina tutte le chiavi protette per il volume.

Se un volume non crittografato dispone di protezione delle chiavi, quando **DeleteKeyProtectors** viene eseguito correttamente il volume ripristina un file system NTFS file system.

Se il volume non è ancora completamente decrittografato, usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di eseguire **DeleteKeyProtectors** per assicurarsi che parti crittografate del volume rimangano accessibili.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.



| Codice/valore restituito                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ CHIAVE \_ RICHIESTA**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | L'ultima protezione con chiave per un volume parzialmente o completamente crittografato non può essere rimossa se sono abilitate le protezione con chiave. Usare [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) prima di rimuovere l'ultima protezione della chiave per assicurarsi che parti crittografate del volume rimangano accessibili. <br/> |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ BOUND \_ ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Non è possibile eliminare le chiavi di protezione perché una di esse viene usata per sbloccare automaticamente il volume. <br/> Usare [**DisableAutoUnlock per**](disableautounlock-win32-encryptablevolume.md) disabilitare lo sblocco automatico prima di eseguire questo metodo.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

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

 

 
