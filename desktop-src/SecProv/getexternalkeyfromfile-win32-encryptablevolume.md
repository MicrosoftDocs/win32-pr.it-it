---
description: Restituisce la chiave esterna da un file.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Metodo GetExternalKeyFromFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316113"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Metodo GetExternalKeyFromFile della \_ classe EncryptableVolume Win32

Il metodo **GetExternalKeyFromFile** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) restituisce la chiave esterna da un file creato da [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dato il percorso del file.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PathWithFileName* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il percorso del file contenente una chiave esterna.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di byte che rappresenta la chiave esterna a 256 bit contenuta nel file che può essere utilizzata per sbloccare un volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Il file non contiene una chiave esterna.<br/>  |
| <dl> <dt>**Errore \_ FILE \_ non \_ trovato**</dt> <dt>2147942402 (0x80070002)</dt> </dl> | Impossibile trovare il file nel percorso specificato.<br/> |



 

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

 

 
