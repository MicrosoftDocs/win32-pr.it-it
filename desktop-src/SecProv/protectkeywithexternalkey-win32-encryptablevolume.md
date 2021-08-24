---
description: Protegge la chiave di crittografia del volume con una chiave esterna a 256 bit.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Metodo ProtectKeyWithExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 63ef4f998d576ecf2931af529a0ff6710a54513cc0d19027421c160bbdcd4cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004419"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithExternalKey della classe \_ EncryptableVolume Win32

Il **metodo ProtectKeyWithExternalKey** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume con una chiave esterna a 256 bit. Questa chiave esterna può essere usata per ripristinare gli errori di autenticazione di altre chiavi di protezione (ad esempio, TPM).

Usare il [**metodo SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) per salvare questa chiave esterna in un file. I dispositivi di memoria USB che contengono questa chiave esterna possono essere usati come chiave di avvio o di ripristino all'avvio del computer.

Per il volume viene creata una protezione con chiave di tipo "Chiave esterna".

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica un identificatore assegnato dall'utente per questa protezione della chiave. Se questo parametro non viene specificato, viene usato un valore vuoto.

</dd> <dt>

*ExternalKey* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit usata per sbloccare il volume.

Se non viene specificata alcuna chiave esterna, ne viene generata una in modo casuale. Usare il [**metodo GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) per ottenere la chiave generata in modo casuale.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco usato per gestire una protezione con chiave di volume crittografata.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione della chiave viene scritta in per ogni metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro ExternalKey* viene fornito ma non è una matrice di dimensioni 4.<br/>            |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/>                                                             |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/> |



 

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

 

 
