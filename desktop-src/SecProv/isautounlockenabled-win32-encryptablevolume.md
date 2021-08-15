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
ms.openlocfilehash: 19437bf40d27bea87103beecfbe8bee71e404c054ace46cb9728f7ac992b5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891912"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Metodo IsAutoUnlockEnabled della classe \_ EncryptableVolume Win32

Il metodo **IsAutoUnlockEnabled** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se il volume viene sbloccato automaticamente al momento del montaggio, ad esempio quando i dispositivi di memoria rimovibile sono connessi al computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsAutoUnlockEnabled* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Valore booleano che è true se la chiave esterna usata per sbloccare automaticamente il volume esiste ed è stata archiviata nel volume del sistema operativo attualmente in esecuzione, in caso contrario è false.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco che contiene l'ID di protezione della chiave del volume crittografato associato se *IsAutoUnlockEnabled* è true.

Se *IsAutoUnlockEnabled è* false, *VolumeKeyProtectorID* è una stringa vuota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                     | Descrizione                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | Il metodo è stato eseguito correttamente.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | Non è possibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.<br/>      |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
