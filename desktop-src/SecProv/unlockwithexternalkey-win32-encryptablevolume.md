---
description: Usa una chiave esterna fornita per accedere al contenuto di un volume di dati.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Metodo UnlockWithExternalKey della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a61e85608e8ed0f3e5b014d015ce7d59c4f01c8d97ab9092864fe9bb338833ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004219"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithExternalKey della classe \_ EncryptableVolume Win32

Il **metodo UnlockWithExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa una chiave esterna fornita per accedere al contenuto di un volume di dati.

La chiave di crittografia del volume deve essere protetta con una o più protezione con chiave di tipo "Chiave esterna" usando il metodo [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per poter sbloccare il volume con questo metodo.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave esterna* \[ Pollici\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit usata per sbloccare il volume. Questa chiave può essere ottenuta chiamando il [**metodo GetExternalKeyFromFile.**](getexternalkeyfromfile-win32-encryptablevolume.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se il volume è già sbloccato, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                                                       |
| <dl> <dt>**ERRORE \_ NOT \_ FOUND**</dt> <dt>Nessun valore specificato (0x)</dt> </dl>          | Il volume non dispone di una protezione con chiave di tipo "Chiave esterna".<br/>                                                             |
| <dl> <dt>**ERRORE \_ INVALID \_ PASSWORD**</dt> <dt>Nessun valore specificato (0x)</dt> </dl>   | Esistono una o più protezione con chiave di tipo "Chiave esterna", ma il parametro *ExternalKey* specificato non è in grado di sbloccare il volume.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il *parametro ExternalKey* non è una matrice di dimensioni 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                |



 

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

 

 
