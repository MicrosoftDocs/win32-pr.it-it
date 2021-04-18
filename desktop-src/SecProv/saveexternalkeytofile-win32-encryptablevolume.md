---
description: Scrive la chiave esterna associata alla protezione con chiave del volume specificata in un file di sistema, nascosto o di sola lettura nella cartella specificata.
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
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314671"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a>Metodo SaveExternalKeyToFile della \_ classe EncryptableVolume Win32

Il metodo **SaveExternalKeyToFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) scrive la chiave esterna associata alla protezione con chiave del volume specificata in un file di sistema, nascosto o di sola lettura nella cartella specificata.

Questo metodo è applicabile solo per le protezioni con chiave di tipo "chiave esterna" o "TPM e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*Percorso* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che contiene il percorso del volume o della cartella in cui salvare la chiave esterna associata alla protezione con chiave specificata. Questo percorso non include il nome del file, che è interno e può variare da una versione all'altra. Usare **GetExternalKeyFileName** per ottenere il nome del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>  | Il volume è bloccato.<br/>                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave del tipo "chiave esterna" o "TPM e chiave di avvio".<br/>            |
| <dl> <dt>**Errore \_ PERCORSO \_ non \_ trovato**</dt> <dt>2147942403 (0 x 80070003)</dt> </dl> | Il parametro *path* non fa riferimento a un percorso valido.<br/> Verificare che il nome file non sia incluso nel parametro *path* .<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                      |



 

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

 

 
