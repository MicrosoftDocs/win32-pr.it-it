---
description: Restituisce la versione dei metadati FVE del volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Metodo GetVersion della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0681498a0d075fa22bada520e22c0ae626a4764d1a917f7090b796f05d66b122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891902"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Metodo GetVersion della classe \_ EncryptableVolume Win32

Il **metodo GetVersion** della [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) restituisce la versione dei metadati FVE del volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Versione* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Intero senza segno che indica la versione dei metadati del volume.



| Valore                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl> | Il sistema operativo è sconosciuto.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Windows Formato Vista, ovvero il volume è stato protetto con BitLocker in un computer che esegue Windows Vista.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Windows 7, ovvero il volume è stato protetto con BitLocker in un computer che esegue Windows 7 o il formato dei metadati è stato aggiornato usando il [**metodo UpgradeVolume.**](upgradevolume-win32-encryptablevolume.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se il volume è già sbloccato e non si verificano altri errori, questo metodo restituisce zero.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                       | Il metodo è riuscito.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | Il valore per il *parametro Version* non è valido.<br/> |
| <dl> <dt>**ERRORE \_ DATI \_ NON**</dt> <dt>VALIDI 13 (0xD)</dt> </dl>       | Il driver ha restituito un formato dati non supportato.<br/>     |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
