---
description: Restituisce il nome del file che contiene la chiave esterna.
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Metodo GetExternalKeyFileName della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 20169325377701ce9edf627246bc5bf848c8489e59fdea3a602af3645aac0b14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668021"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a>Metodo GetExternalKeyFileName della classe \_ EncryptableVolume Win32

Il metodo **GetExternalKeyFileName** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) restituisce il nome del file che contiene la chiave esterna, se questa chiave esterna viene salvata in un percorso di file usando il metodo [**SaveExternalKeyToFile.**](saveexternalkeytofile-win32-encryptablevolume.md)

Questo metodo è applicabile solo per le protezione con chiave di tipo "Chiave esterna", "TPM, PIN e chiave di avvio" o "TPM e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco usato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*FileName* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Stringa che specifica il nome con estensione ma senza il percorso del file che contiene la chiave esterna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Chiave esterna", "TPM, PIN e chiave di avvio" o "TPM e chiave di avvio".<br/> |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl> | Il volume è bloccato.<br/>                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                           |



 

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
</dt> <dt>

[**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 
