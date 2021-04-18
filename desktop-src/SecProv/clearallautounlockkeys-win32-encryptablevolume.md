---
description: Rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono utilizzate per sbloccare automaticamente i volumi di dati.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Metodo ClearAllAutoUnlockKeys della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306408"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Metodo ClearAllAutoUnlockKeys della \_ classe EncryptableVolume Win32

Il metodo **ClearAllAutoUnlockKeys** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono usate per sbloccare automaticamente i volumi di dati.

## <a name="syntax"></a>Sintassi


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ \_ volume del sistema operativo**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.<br/>     |



 

## <a name="remarks"></a>Commenti

**ClearAllAutoUnlockKeys** ottiene le stesse funzionalità di esecuzione di [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per ogni volume di dati associato al sistema operativo attualmente in esecuzione, anche per i volumi di dati che non sono attualmente connessi al computer. Rimuove anche eventuali informazioni di sblocco non aggiornate associate a volumi di dati che non esistono più.

Prima di chiamare [**Decrypt**](decrypt-win32-encryptablevolume.md) sul volume del sistema operativo attualmente in esecuzione, usare **ClearAllAutoUnlockKeys** per assicurarsi che le informazioni inserite nel registro di sistema del sistema operativo per sbloccare automaticamente i volumi di dati non siano accessibili in chiaro su disco.

Dopo l'esecuzione corretta di **ClearAllAutoUnlockKeys** , è possibile usare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare tutti i volumi di dati nel computer. Usare [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per abilitare di nuovo lo sblocco automatico di un volume di dati.

Se non vengono restituiti altri errori, **ClearAllAutoUnlockKeys** rimuove dal registro di sistema tutti gli ID di protezione del volume e le chiavi esterne usate per sbloccare automaticamente qualsiasi volume di dati associato al volume del sistema operativo attualmente in esecuzione.

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

 

 
