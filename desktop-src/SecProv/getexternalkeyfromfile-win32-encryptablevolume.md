---
description: Restituisce la chiave esterna da un file.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Metodo GetExternalKeyFromFile della Win32_EncryptableVolume classe
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
ms.openlocfilehash: e2046e64340167a98d838fd5a64324a410b0d0418a740550f9336117e2f1d8d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892429"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a>Metodo GetExternalKeyFromFile della classe \_ EncryptableVolume Win32

Il **metodo GetExternalKeyFromFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) restituisce la chiave esterna da un file creato da [**SaveExternalKeyToFile,**](saveexternalkeytofile-win32-encryptablevolume.md)in base al percorso del file.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PathWithFileName* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa che specifica il percorso del file contenente una chiave esterna.

</dd> <dt>

*Chiave esterna* \[ Cambio\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che rappresenta la chiave esterna a 256 bit contenuta nel file che può essere usata per sbloccare un volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>           | Il file non contiene una chiave esterna.<br/>  |
| <dl> <dt>**ERRORE \_ FILE \_ NON \_ TROVATO 2147942402**</dt> <dt>(0x80070002)</dt> </dl> | Impossibile trovare il file nel percorso specificato.<br/> |



 

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

 

 
