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
ms.openlocfilehash: ce3a6bbb396136b128e084da0e64a79ad2f403217d8ac51dcf67b57941cc4a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004559"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a>Metodo DisableAutoUnlock della classe \_ EncryptableVolume Win32

Il **metodo DisableAutoUnlock** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione in modo che un volume di dati non sia sbloccato automaticamente quando viene montato, ad esempio quando i dispositivi di memoria rimovibile sono connessi al computer.

Se lo sblocco automatico è disabilitato o sospeso, è necessario usare i metodi [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) o [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) per sbloccare il volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/>                                                       |
| <dl> <dt> **FVE \_ E VOLUME NOT \_ \_ \_ BOUND**</dt> <dt>2150694935 (0x80310017)</dt> </dl> | Lo sblocco automatico nel volume è disabilitato.<br/>                                   |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl>   | Il metodo non può essere eseguito per il volume del sistema operativo attualmente in esecuzione.<br/>      |



 

## <a name="remarks"></a>Commenti

Se non vengono restituiti errori, questo metodo rimuove dal Registro di sistema gli ID protezione volume e le chiavi esterne usate per sbloccare automaticamente il volume.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
