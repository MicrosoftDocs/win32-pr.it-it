---
description: Avvia la decrittografia di un volume completamente crittografato o riprende la decrittografia di un volume parzialmente crittografato.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Metodo Decrypt della classe Win32_EncryptableVolume (Infocard.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e9018cfab8bea6c149c4771a54dbe55a62afafd447f4db2e162aa76d183c28ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004629"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Metodo Decrypt della classe \_ EncryptableVolume Win32

Il **metodo Decrypt** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) inizia la decrittografia di un volume completamente crittografato o riprende la decrittografia di un volume parzialmente crittografato.

Quando la decrittografia viene sospesa o in corso, questo metodo si comporta come [**ResumeConversion.**](resumeconversion-win32-encryptablevolume.md) Quando la crittografia viene sospesa o in corso, questo metodo ripristina la crittografia e inizia la decrittografia. Al termine della decrittografia, tutte le protezione con chiave in questo volume vengono rimosse dal sistema e il volume viene convertito in un file system NTFS file system.

> [!Note]  
> Se il disco è crittografato con hardware, il metodo **Decrypt** imposta lo stato della banda su "always unlocked", rimuove tutti i metadati associati e azzerare l'ID di sicurezza per l'unità.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Questo metodo viene restituito immediatamente. Se il volume è già completamente decrittografato e non esistono altri errori, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl>      | Il volume è bloccato.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ AUTOUNLOCK \_ ENABLED 2150694953**</dt> <dt>(0x80310029)</dt> </dl> | Questo volume non può essere decrittografato perché sono disponibili chiavi usate per sbloccare automaticamente i volumi di dati. <br/> Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere queste chiavi.<br/> |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

La chiamata **al metodo Decrypt** lascia i dati non protetti.

Se lo stato di protezione del volume è 1 (PROTECTION ON) prima dell'uso di questo metodo, il completamento corretto di questo metodo imposta lo stato di protezione su 0 (PROTECTION OFF), perché per definizione un volume parzialmente crittografato non è protetto.

## <a name="remarks"></a>Commenti

Se il volume non è già completamente decrittografato, l'esecuzione di **Decrypt** fa sì che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la decrittografia è in corso e mostra la percentuale del volume che rimane crittografata.

Se lo stato di protezione del volume è "on" prima dell'esecuzione di questo metodo, l'esecuzione di questo metodo imposta lo stato di protezione su "off", perché per definizione un volume parzialmente crittografato non è protetto.

Se questo metodo viene eseguito nel volume del sistema operativo attualmente in esecuzione e questo volume del sistema operativo viene usato per sbloccare automaticamente i volumi di dati (vedere il metodo [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), è necessario chiamare prima il metodo [**ClearAllAutoUnlockKeys.**](clearallautounlockkeys-win32-encryptablevolume.md)

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>Infocard.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
