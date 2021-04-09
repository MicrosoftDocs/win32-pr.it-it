---
description: Rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Metodo DisableAutoUnlock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882078"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Metodo DisableAutoUnlock della \_ classe EncryptableVolume Win32

Il metodo **DisableAutoUnlock** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione, in modo che un volume di dati non venga sbloccato automaticamente quando viene montato, ad esempio quando i dispositivi di memoria rimovibili sono connessi al computer.

Se lo sblocco automatico è disabilitato o sospeso, è necessario utilizzare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare il volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/>                                                       |
| <dl> <dt> **FVE \_ E \_ volume \_ non \_ associato**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | Lo sblocco automatico sul volume è disabilitato.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.<br/>      |



 

## <a name="remarks"></a>Commenti

Se non vengono restituiti errori, questo metodo rimuove dal registro di sistema tutti gli ID di protezione del volume e le chiavi esterne usate per sbloccare automaticamente il volume.

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

 

 
