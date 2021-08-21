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
ms.openlocfilehash: 3f5a8a9664c48451083808cc0e7a5f3448dbd5a87756503add896e278845421b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892898"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo ChangeExternalKey della classe \_ EncryptableVolume Win32

Il **metodo ChangeExternalKey** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) modifica una chiave esterna associata a un volume crittografato.

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

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco usato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

 *NewExternalKey* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit usata per sbloccare il volume.

</dd> <dt>

*NewVolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave del volume crittografata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                    | Il *parametro NewExternalKey* non è una matrice di dimensioni 32.<br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl>           | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>          | In questo computer è disponibile un CD/DVD di avvio. Rimuovere il CD/DVD e riavviare il computer.<br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ PROTEZIONE NON TROVATA \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ TIPO DI PROTEZIONE \_ \_ 2150694970**</dt> <dt>NON VALIDO (0x8031003A)</dt> </dl> | Il *parametro VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "Numerical Password" o "External Key". Usare il [**metodo ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) o [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare una protezione con chiave del tipo appropriato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo può essere usato per modificare la chiave esterna per qualsiasi protezione con chiave che usa una chiave esterna.

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

 

 




