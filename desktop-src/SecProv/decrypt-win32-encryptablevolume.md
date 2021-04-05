---
description: Inizia la decrittografia di un volume completamente crittografato oppure riprende la decrittografia di un volume parzialmente crittografato.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Metodo Decrypt della classe Win32_EncryptableVolume (infocard. h)
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
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882081"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a>Metodo Decrypt della \_ classe Win32 EncryptableVolume

Il metodo **Decrypt** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inizia la decrittografia di un volume completamente crittografato oppure riprende la decrittografia di un volume parzialmente crittografato.

Quando la decrittografia viene sospesa o in corso, il comportamento di questo metodo è uguale a quello di [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Quando la crittografia viene sospesa o in corso, questo metodo ripristina la crittografia e inizia la decrittografia. Al termine della decrittografia, tutte le protezioni con chiave presenti in questo volume vengono rimosse dal sistema e il volume viene convertito in un file system NTFS standard.

> [!Note]  
> Se il disco è crittografato con hardware, il metodo **Decrypt** imposta lo stato della banda su "always Unlocked", rimuove tutti i metadati associati e azzera l'ID di sicurezza per l'unità.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 Decrypt();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Questo metodo restituisce immediatamente un risultato. Se il volume è già completamente decrittografato e non esistono altri errori, questo metodo restituisce 0.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                   |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>      | Il volume è bloccato.<br/>                                                                                                                                                                                                        |
| <dl> <dt>**FVE \_ \_Sblocco automatico \_ abilitato**</dt> <dt>2150694953 (0x80310029)</dt> </dl> | Non è possibile decrittografare questo volume perché sono disponibili le chiavi usate per sbloccare automaticamente i volumi di dati. <br/> Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere queste chiavi.<br/> |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

La chiamata al metodo **Decrypt** lascia i dati non protetti.

Se lo stato di protezione del volume è 1 (PROTECTION ON) prima che questo metodo venga usato, il completamento di questo metodo modifica lo stato di protezione in 0 (PROTECTION OFF), poiché per definizione un volume parzialmente crittografato non è protetto.

## <a name="remarks"></a>Commenti

Se il volume non è già completamente decrittografato, l'esecuzione di **decrittografia** fa sì che [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indichi che la decrittografia è in corso e Mostra la percentuale del volume che rimane crittografato.

Se lo stato di protezione del volume è "on" prima dell'esecuzione di questo metodo, l'esecuzione di questo metodo imposta lo stato di protezione su "off", poiché per definizione un volume parzialmente crittografato non è protetto.

Se questo metodo viene eseguito nel volume del sistema operativo attualmente in esecuzione e questo volume del sistema operativo viene usato per sbloccare automaticamente i volumi di dati (vedere il metodo [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), è necessario chiamare prima il metodo [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/>                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>Infocard. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
