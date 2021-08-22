---
description: Scrive la chiave esterna associata alla protezione della chiave del volume specificata in un file di sistema nascosto di sola lettura nella cartella specificata.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Metodo SaveExternalKeyToFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 02269d2b2339ebc8a2b6022bc5f02e63710d496e768be09dad9993c177ed5de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004289"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Metodo SaveExternalKeyToFile della classe \_ EncryptableVolume Win32

Il metodo **SaveExternalKeyToFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) scrive la chiave esterna associata alla protezione della chiave del volume specificata in un file di sistema nascosto di sola lettura nella cartella specificata.

Questo metodo è applicabile solo per le chiavi di protezione di tipo "Chiave esterna" o "TPM e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco usato per gestire una protezione con chiave di volume crittografata.

</dd> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa contenente il percorso del volume o della cartella in cui deve essere salvata la chiave esterna associata alla protezione della chiave specificata. Questo percorso non include il nome del file, che è interno e può cambiare da versione a versione. Usare **GetExternalKeyFileName** per ottenere il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | Il volume è bloccato.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Il *parametro VolumeKeyProtectorID* non fa riferimento a una protezione della chiave di tipo "Chiave esterna" o "TPM e chiave di avvio".<br/>            |
| <dl> <dt>**ERRORE \_ PERCORSO \_ NON \_ TROVATO**</dt> 2147942403 <dt>(0x80070003)</dt> </dl> | Il *parametro Path* non fa riferimento a un percorso valido.<br/> Assicurarsi che il nome del file non sia incluso nel *parametro Path.*<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                      |



 

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
