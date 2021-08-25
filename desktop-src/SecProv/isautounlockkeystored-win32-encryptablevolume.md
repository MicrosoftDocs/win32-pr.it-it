---
description: Indica se nel volume del sistema operativo attualmente in esecuzione sono presenti chiavi esterne o informazioni correlate che possono essere usate per sbloccare automaticamente i volumi di dati.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Metodo IsAutoUnlockKeyStored della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c28f8357edd88322f6f4498fd1e5b7156eeeff0b67d53b4d759c6935f4e9f9eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906311"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Metodo IsAutoUnlockKeyStored della classe \_ EncryptableVolume Win32

Il metodo **IsAutoUnlockKeyStored** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se nel volume del sistema operativo attualmente in esecuzione sono presenti chiavi esterne o informazioni correlate che possono essere usate per sbloccare automaticamente i volumi di dati.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsAutoUnlockKeyStored* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

È **true** se tutte le informazioni che possono essere usate per sbloccare automaticamente i volumi di dati vengono archiviate nel Registro di sistema del volume del sistema operativo attualmente in esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                   | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | Il metodo è stato eseguito correttamente.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | Il metodo può essere eseguito solo per il volume del sistema operativo attualmente in esecuzione.<br/>     |



 

## <a name="remarks"></a>Commenti

Usare [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) per rimuovere tutte le informazioni di sblocco dal volume del sistema operativo attualmente in esecuzione.

Le informazioni usate per sbloccare un volume vengono archiviate quando si esegue [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) per un volume di dati mentre il volume del sistema operativo attualmente in esecuzione è in esecuzione.

**IsAutoUnlockKeyStored** è diverso da [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) perché anche se lo sblocco automatico è disabilitato per tutti i volumi di dati attualmente connessi al computer, è possibile che siano ancora presenti informazioni di sblocco associate a volumi di dati disconnessi o volumi di dati che non esistono più.

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

 

 
