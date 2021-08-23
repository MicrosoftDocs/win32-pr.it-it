---
description: Recupera la chiave esterna per una protezione con chiave specificata.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Metodo GetKeyProtectorExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f6db531e28880c6b47cb41d87769917a524965984e2a2fc1099f0d0aa65095f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667891"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorExternalKey della classe \_ EncryptableVolume Win32

Il **metodo GetKeyProtectorExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera la chiave esterna per una determinata protezione della chiave del tipo appropriato.

L'identificatore della protezione delle chiavi deve fare riferimento a una protezione con chiave di tipo "Chiave esterna", "TPM e PIN e chiave di avvio" o "TPM e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco usato per gestire una protezione con chiave di volume crittografata.

</dd> <dt>

*ExternalKey* \[ Cambio\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit che può essere usata per sbloccare il volume corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Chiave esterna", "TPM e PIN e chiave di avvio" o "TPM e chiave di avvio".<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                           |



 

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

 

 
