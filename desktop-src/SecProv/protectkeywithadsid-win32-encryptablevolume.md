---
description: Protegge la chiave di crittografia del volume utilizzando un ID di sicurezza Active Directory (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Metodo ProtectKeyWithAdSid della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315339"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithAdSid della \_ classe EncryptableVolume Win32

Il metodo **ProtectKeyWithAdSid** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando un ID di sicurezza Active Directory (SID).

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica un identificatore assegnato dall'utente per la protezione con chiave. Se questo parametro non è specificato, viene utilizzato un valore blank.

</dd> <dt>

*SidString* \[ in\]
</dt> <dd>

Stringa che contiene il SID Active Directory usato per proteggere la chiave di crittografia.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Flag che modificano il comportamento della funzione. Può corrispondere a uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ \_Flag ng \_ DPAPI \_ None**</dt> <dt>0x0000</dt> </dl>                                                                   | Nessun effetto.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ Lo \_ sblocco del flag ng DPAPI \_ \_ \_ come \_ \_ account del servizio**</dt> <dt>0x0001</dt> </dl> | Specifica che la protezione basata su SID è stata protetta per un account del servizio. Se questo flag è specificato, il chiamante deve verificare che sia in esecuzione come account del servizio appropriato prima di chiamare [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (eliminando temporaneamente la rappresentazione, ad esempio).<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Identificatore univoco associato alla protezione creata. È possibile usare questa stringa per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)

Per impostazione predefinita, non è possibile aggiungere un account Active Directory o un gruppo di protezione in modalità remota. È necessario abilitare la delega vincolata sul controller di dominio e sul computer di origine. Nel controller di dominio seguire questa procedura:

1.  Avviare Server Manager
2.  Selezione dei computer nei ruoli Active Directory
3.  Selezionare il computer client di destinazione e fare clic con il pulsante destro
4.  Selezionare la scheda delega
5.  Selezionare il pulsante di opzione "considera attendibile il computer per la delega solo ai servizi specificati"
6.  Selezionare il pulsante di opzione "USA solo Kerberos"
7.  Fare clic su Aggiungi.
8.  Selezionare "utenti o computer"
9.  Selezionare host/come nome dell'entità servizio

Eseguire i passaggi da 3 a 9 nel computer di origine.

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

 

 
