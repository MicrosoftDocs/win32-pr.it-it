---
description: Recupera l'identificatore di sicurezza e i flag utilizzati per proteggere una chiave.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Metodo GetKeyProtectorAdSidInformation della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334004"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorAdSidInformation della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectorAdSidInformation** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) recupera l'identificatore di sicurezza e i flag utilizzati per proteggere una chiave.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa che può essere usato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*SidString* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che contiene l'ID di sicurezza (SID).

</dd> <dt>

*Flag* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Flag che modificano il comportamento della funzione. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ \_Flag ng \_ DPAPI \_ None**</dt> <dt>0x0000</dt> </dl>                                                                   | Nessun effetto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ Lo \_ sblocco del flag ng DPAPI \_ \_ \_ come \_ \_ account del servizio**</dt> <dt>0x0001</dt> </dl> | Specifica che la protezione basata su SID è stata protetta per un account del servizio. Se questo flag è specificato, il chiamante deve verificare che sia in esecuzione come account del servizio appropriato prima di chiamare [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (eliminando temporaneamente la rappresentazione, ad esempio).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 Enterprise, \[ solo app desktop Windows 8 Pro\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
