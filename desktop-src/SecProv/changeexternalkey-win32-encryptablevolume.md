---
description: Modifica una chiave esterna associata a un volume crittografato.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Metodo ChangeExternalKey della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316121"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo ChangeExternalKey della \_ classe EncryptableVolume Win32

Il metodo **ChangeExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifica una chiave esterna associata a un volume crittografato.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

 *NewExternalKey* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume.

</dd> <dt>

*NewVolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco aggiornato utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | Il parametro *NewExternalKey* non è una matrice di dimensioni pari a 32.<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ \_ CDDVD di avvio**</dt> <dt>2150694960 (0x80310030)</dt> </dl>          | Nel computer è presente un CD/DVD di avvio. Rimuovere il CD/DVD e riavviare il computer.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo di protezione non valido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical password" o "External Key". Usare il metodo [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per modificare la chiave esterna per qualsiasi protezione con chiave che utilizza una chiave esterna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




