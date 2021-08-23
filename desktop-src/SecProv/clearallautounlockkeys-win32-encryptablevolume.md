---
description: Rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono usate per sbloccare automaticamente i volumi di dati.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Metodo ClearAllAutoUnlockKeys della Win32_EncryptableVolume
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
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668171"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Metodo ClearAllAutoUnlockKeys della classe \_ EncryptableVolume Win32

Il **metodo ClearAllAutoUnlockKeys** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione che vengono usate per sbloccare automaticamente i volumi di dati.

## <a name="syntax"></a>Sintassi


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.<br/>     |



 

## <a name="remarks"></a>Commenti

**ClearAllAutoUnlockKeys** ottiene le stesse funzionalità dell'esecuzione di [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) per ogni volume di dati che sia mai stato associato al sistema operativo attualmente in esecuzione, anche per i volumi di dati che non sono attualmente connessi al computer. Rimuove anche le informazioni di sblocco non aggiornate associate ai volumi di dati che non esistono più.

Prima di chiamare [**Decrypt**](decrypt-win32-encryptablevolume.md) sul volume del sistema operativo attualmente in esecuzione, usare **ClearAllAutoUnlockKeys** per assicurarsi che le informazioni inserite nel Registro di sistema operativo per sbloccare automaticamente i volumi di dati non siano accessibili in modalità non crittografata su disco.

Dopo **l'esecuzione di ClearAllAutoUnlockKeys,** è possibile usare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare tutti i volumi di dati nel computer. Usare [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per abilitare nuovamente lo sblocco automatico di un volume di dati.

Se non vengono restituiti altri errori, **ClearAllAutoUnlockKeys** rimuove dal Registro di sistema tutti gli ID di protezione del volume e le chiavi esterne usati per sbloccare automaticamente qualsiasi volume di dati che sia mai stato associato al volume del sistema operativo attualmente in esecuzione.

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

 

 
