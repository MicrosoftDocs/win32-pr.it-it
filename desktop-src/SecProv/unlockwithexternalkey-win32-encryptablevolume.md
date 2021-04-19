---
description: Usa una chiave esterna fornita per accedere al contenuto di un volume di dati.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Metodo UnlockWithExternalKey della classe Win32_EncryptableVolume
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
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317683"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithExternalKey della \_ classe EncryptableVolume Win32

Il metodo **UnlockWithExternalKey** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa una chiave esterna fornita per accedere al contenuto di un volume di dati.

La chiave di crittografia del volume deve essere stata protetta con una o più protezioni con chiave di tipo "chiave esterna" usando il metodo [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per poter sbloccare il volume con questo metodo.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ExternalKey* \[ in\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume. Questa chiave può essere ottenuta chiamando il metodo [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se il volume è già sbloccato, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                                                       |
| <dl> <dt>**Errore \_ NON \_**</dt> è stato trovato <dt>alcun valore specificato (0x)</dt> </dl>          | Il volume non dispone di una protezione con chiave di tipo "chiave esterna".<br/>                                                             |
| <dl> <dt>**Errore \_ La \_ password**</dt> non è valida. <dt>nessun valore specificato (0x)</dt> </dl>   | Sono presenti una o più protezioni con chiave di tipo "chiave esterna", ma il parametro *ExternalKey* specificato non è in grado di sbloccare il volume.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il parametro *ExternalKey* non è una matrice di dimensioni 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                |



 

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

 

 
