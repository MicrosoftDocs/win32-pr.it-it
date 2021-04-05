---
description: Consente di sbloccare automaticamente un volume di dati quando viene montato il volume.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Metodo EnableAutoUnlock della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882069"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a>Metodo EnableAutoUnlock della \_ classe EncryptableVolume Win32

Il metodo **EnableAutoUnlock** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) consente di sbloccare automaticamente un volume di dati quando viene montato il volume.

Lo sblocco automatico salva una chiave esterna nel sistema operativo in grado di sbloccare automaticamente il volume nel volume del sistema operativo attualmente in esecuzione.

Per usare questo metodo, il volume del sistema operativo deve essere già protetto da Crittografia unità BitLocker o deve avere la crittografia in corso. Inoltre, è necessario che esista già una chiave esterna per il volume di dati. Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) per creare la chiave esterna che può sbloccare automaticamente il volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica la protezione con chiave del tipo "chiave esterna" utilizzata per sbloccare automaticamente il volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                           | Descrizione                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                        |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>          | Il volume è bloccato.<br/>                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>          | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                   | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave valida del tipo "External Key".<br/>                                                          |
| <dl> <dt>**FVE \_ E \_ non \_ il \_ VOLUME di dati**</dt> <dt>2150694937 (0x80310019)</dt> </dl>       | Impossibile eseguire il metodo per il volume del sistema operativo attualmente in esecuzione.<br/>                                                                                       |
| <dl> <dt>**FVE \_ \_Sistema operativo E \_ non \_ protetto**</dt> <dt>2150694944 (0x80310020)</dt> </dl>      | Il metodo non può essere eseguito se il volume del sistema operativo attualmente in esecuzione non è protetto da Crittografia unità BitLocker o se la crittografia non è in corso.<br/> |
| <dl> <dt> **FVE \_ E \_ volume \_ binding \_ già**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Lo sblocco automatico sul volume è stato precedentemente abilitato.<br/>                                                                                                    |



 

## <a name="remarks"></a>Commenti

Data una protezione con chiave del volume valida del tipo "chiave esterna", la chiave esterna a 256 bit correlata viene estratta dalla protezione e archiviata nel registro di sistema del sistema operativo attualmente in esecuzione, insieme all'ID della protezione con chiave del volume.

Se la chiave esterna associata all'ID della protezione con chiave del volume viene eliminata, la funzionalità di sblocco automatico del volume viene disabilitata o sospesa.

> [!Note]  
> I supporti rimovibili non sono attualmente supportati.

 

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

 

 
