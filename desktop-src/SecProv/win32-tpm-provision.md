---
description: Tenta di effettuare il provisioning del TPM in uno stato completamente pronto e, se non è già di proprietà, diventa proprietario del TPM.
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm::P rovision
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5153672d91c88597676f65b53a93de6ffac9f4989dd9e231c87a3b7947b1d657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890809"
---
# <a name="win32_tpmprovision-method"></a>Metodo \_ Win32 Tpm::P rovision

Tenta di effettuare il provisioning del TPM in uno stato completamente pronto e, se non è già di proprietà, diventa proprietario del TPM. L'esecuzione di questo metodo è dispendiosa perché esegue molti controlli. È consigliabile che le applicazioni usino questo metodo solo quando necessario.

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ForceClear \_ Consentito* \[ in\]
</dt> <dd>

Se impostato su **TRUE,** il metodo può richiedere operazioni di presenza fisica per cancellare il TPM. Se impostato su **FALSE,** il metodo non richiederà un'operazione di presenza fisica per cancellare il TPM.

</dd> <dt>

*PhysicalPresencePrompts \_ Consentito* \[ in\]
</dt> <dd>

Se impostato su **TRUE,** il metodo può richiedere operazioni di presenza fisica che richiedono il coinvolgimento dell'utente durante il processo di avvio per confermare la modifica dello stato del TPM.

</dd> <dt>

*Informazioni* \[ Cambio\]
</dt> <dd>

Restituisce una maschera di bit con tutte le informazioni disponibili per il provisioning completo del TPM. I valori di maschera come INFORMATION \_ REBOOT indicano che la chiamata al metodo deve avviare un riavvio per spostare in avanti il processo di provisioning.

Il *parametro Information* può essere costituito da valori seguenti.



| Valore                                                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**INFORMAZIONI \_ Arresto**</dt> <dt>0x00000002</dt> </dl>                                                 | È necessario riavviare la piattaforma (arresto).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**INFORMAZIONI \_ RIAVVIARE**</dt> <dt>0x00000004</dt> </dl>                                                       | È necessario riavviare la piattaforma (riavvio).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ FORCE \_ CLEAR**</dt> <dt>0x00000008</dt> </dl>                          | Il TPM è già di proprietà. È necessario cancellare il TPM o importare il valore di autorizzazione del proprietario del TPM.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**INFORMAZIONI \_ PRESENZA \_ FISICA**</dt> <dt>0x00000010</dt> </dl>                     | La presenza fisica è necessaria per effettuare il provisioning del TPM.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**INFORMAZIONI \_ Attivazione \_ TPM**</dt> <dt>0x00000020</dt> </dl>                                    | Il TPM è disabilitato o disattivato.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ TAKE \_ OWNERSHIP**</dt> <dt>0x00000040</dt> </dl>                 | La proprietà del TPM è stata presa.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ CREATE \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Una chiave di verifica dell'approvazione (EK) esiste nel TPM. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt> </dl>                                 | L'autorizzazione del proprietario del TPM non è archiviata correttamente nel Registro di sistema.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ SRK \_ AUTH**</dt> <dt>0x000000200</dt> </dl>                                  | Il Archiviazione di autorizzazione della chiave radice radice (SRK) non è uguale a zero.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ DISABLE OWNER CLEAR \_ \_ 0x00000400**</dt> <dt></dt> </dl> | Se il sistema operativo è configurato per disabilitare la cancellazione del TPM con il valore di autorizzazione proprietario TPM e il TPM non è ancora stato configurato per impedire la cancellazione del TPM con il valore di autorizzazione proprietario TPM .<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | Le informazioni del Registro di sistema del sistema operativo relative alla chiave radice Archiviazione TPM non corrispondono a Archiviazione TPM.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | Il flag permanente TPM per consentire la lettura del valore pubblico Archiviazione chiave radice non è impostato.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**INFORMAZIONI \_ CONTATORE \_ DI \_ AVVIO TPM**</dt> <dt>0x00002000</dt> </dl>                       | Il contatore monotona incrementato durante l'avvio non è stato creato.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ AD \_ BACKUP**</dt> <dt>0x00004000</dt> </dl>                                | Non è stato eseguito il backup dell'autorizzazione del proprietario del TPM in Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ AD BACKUP PHASE I \_ \_ \_ 0x00008000**</dt> <dt></dt> </dl>      | La prima parte dell'archiviazione delle informazioni di autorizzazione del proprietario del TPM in Active Directory è in corso.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**INFORMAZIONI \_ TPM \_ AD BACKUP PHASE \_ \_ \_ II**</dt> <dt>0x00010000</dt> </dl>   | La seconda parte dell'archiviazione delle informazioni di autorizzazione del proprietario del TPM in Active Directory è in corso.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**INFORMAZIONI \_ CONFIGURAZIONE \_ LEGACY**</dt> <dt>0x00020000</dt> </dl>            | Windows Criteri di gruppo è configurato per non archiviare alcuna autorizzazione del proprietario del TPM, quindi il TPM non può essere completamente pronto.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**INFORMAZIONI \_ Certificato \_ EK**</dt> <dt>0x00040000</dt> </dl>                              | Il certificato EK non è stato letto dalla RAM NV TPM e archiviato nel Registro di sistema. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**INFORMAZIONI \_ Log eventi TCG \_ \_ 0x00080000**</dt> <dt></dt> </dl>                                | Il registro eventi TCG è vuoto o non può essere letto. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**INFORMAZIONI \_ NON \_ RIDOTTO**</dt> <dt>0x00100000</dt> </dl>                                       | Il TPM non è di proprietà.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**INFORMAZIONI \_ ERRORE \_ GENERICO**</dt> <dt>0x00200000</dt> </dl>                                 | Si è verificato un errore, ma non è specifico di una determinata attività.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**INFORMAZIONI \_ CONTATORE \_ \_ BLOCCO DISPOSITIVO**</dt> <dt>0X00400000</dt> </dl>              | Il contatore di blocco del dispositivo non è stato creato.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi [di base TPM.](../tbs/tbs-return-codes.md)

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
