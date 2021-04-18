---
description: Indica se il volume viene sbloccato automaticamente quando viene montato.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Metodo IsAutoUnlockEnabled della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306389"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Metodo IsAutoUnlockEnabled della \_ classe EncryptableVolume Win32

Il metodo **IsAutoUnlockEnabled** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il volume viene sbloccato automaticamente quando viene montato, ad esempio quando i dispositivi di memoria rimovibili sono connessi al computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsAutoUnlockEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Valore booleano che è true se la chiave esterna utilizzata per sbloccare automaticamente il volume esiste ed è stata archiviata nel volume del sistema operativo attualmente in esecuzione; in caso contrario, è false.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco che contiene l'ID della protezione con chiave del volume crittografato associato se *IsAutoUnlockEnabled* è true.

Se *IsAutoUnlockEnabled* è false, *VolumeKeyProtectorID* è una stringa vuota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                     | Descrizione                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | Il metodo è stato eseguito correttamente.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.<br/>      |



 

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

 

 
