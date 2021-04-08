---
description: Tenta di effettuare il provisioning del TPM in uno stato completamente pronto e assume la proprietà di TPM se non è già di proprietà.
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm::P metodo rovision
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
ms.openlocfilehash: 198d7b02b1813002ce55d175ad016ace23ee7da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884274"
---
# <a name="win32_tpmprovision-method"></a>\_TPM Win32::P metodo rovision

Tenta di effettuare il provisioning del TPM in uno stato completamente pronto e assume la proprietà di TPM se non è già di proprietà. Questo metodo è costoso da eseguire perché esegue molti controlli. Le applicazioni consigliate utilizzano questo metodo solo quando necessario.

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

Se impostato su **true** , il metodo può richiedere operazioni di presenza fisica per cancellare il TPM. Se è impostato su **false**, il metodo non richiederà un'operazione di presenza fisica per cancellare il TPM.

</dd> <dt>

*PhysicalPresencePrompts \_ Consentito* \[ in\]
</dt> <dd>

Se impostato su **true** , il metodo può richiedere operazioni di presenza fisica che richiedono il coinvolgimento dell'utente durante il processo di avvio per confermare la modifica dello stato del TPM.

</dd> <dt>

*Informazioni* \[ su out\]
</dt> <dd>

Restituisce una maschera di base della quantità di informazioni disponibile per il provisioning completo del TPM. Mask values like INFORMATION \_ reboot indica che la chiamata al metodo deve avviare un riavvio per spostare il processo di provisioning in avanti.

Il parametro *Information* può essere costituito dai valori seguenti.



| Valore                                                                                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**Informazioni \_ su ARRESTA**</dt> <dt>0x00000002</dt> </dl>                                                 | Il riavvio della piattaforma è obbligatorio (arresto).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**Informazioni \_ su Riavvia**</dt> <dt>0x00000004</dt> </dl>                                                       | Il riavvio della piattaforma è obbligatorio (riavvio).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**Informazioni \_ su 0x00000008 \_ \_ Clear forzato del TPM**</dt> <dt></dt> </dl>                          | Il TPM è già di proprietà. È necessario cancellare il TPM o importare il valore di autorizzazione del proprietario del TPM.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**Informazioni \_ su \_Presenza fisica**</dt> <dt>0x00000010</dt> </dl>                     | Per eseguire il provisioning del TPM, è necessaria la presenza fisica.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**Informazioni \_ su \_Attivazione**</dt> <dt>0x00000020</dt> TPM </dl>                                    | Il TPM è disabilitato o disattivato.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**Informazioni \_ su \_Accetta \_ Proprietà TPM**</dt> <dt>0x00000040</dt> </dl>                 | È stata acquisita la proprietà del TPM.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**Informazioni \_ su \_Creazione TPM \_**</dt> <dt>0x00000080</dt> </dl>                                | Nel TPM esiste una chiave di verifica dell'autenticità. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**Informazioni \_ su 0x00000100 \_ OWNERAUTH TPM**</dt> <dt></dt> </dl>                                 | L'autorizzazione del proprietario del TPM non è archiviata correttamente nel registro di sistema.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Informazioni \_ su TPM \_ SRK \_ AUTH**</dt> <dt>0x000000200</dt> </dl>                                  | Il valore di autorizzazione della chiave radice di archiviazione (SRK) non è pari a zero.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Informazioni \_ su \_Disabilitare il \_ proprietario \_ 0X00000400 Clear del TPM**</dt> <dt></dt> </dl> | Se il sistema operativo è configurato per disabilitare la cancellazione del TPM con il valore di autorizzazione del proprietario del TPM e il TPM non è ancora stato configurato per impedire la cancellazione del TPM con il valore di autorizzazione del proprietario del TPM.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Informazioni \_ su 0x00000800 \_ SRKPUB TPM**</dt> <dt></dt> </dl>                                          | Le informazioni del registro di sistema del sistema operativo relative alla chiave radice di archiviazione del TPM non corrispondono alla chiave radice di archiviazione TPM.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Informazioni \_ su 0x00001000 \_ \_ SRKPUB Read TPM**</dt> <dt></dt> </dl>                          | Il flag permanente TPM per consentire la lettura del valore pubblico della chiave radice di archiviazione non è impostato.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Informazioni \_ su 0x00002000 \_ \_ contatore avvio TPM**</dt> <dt></dt> </dl>                       | Il contatore monotonic incrementato durante l'avvio non è stato creato.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Informazioni \_ su 0x00004000 \_ \_ backup ad TPM**</dt> <dt></dt> </dl>                                | Non è stato eseguito il backup dell'autorizzazione del proprietario del TPM in Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Informazioni \_ su \_Fase di backup di ad TPM \_ \_ \_ I**</dt> <dt>0x00008000</dt> </dl>      | È in corso la prima parte dello spazio di archiviazione delle informazioni di autorizzazione del proprietario del TPM in Active Directory.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Informazioni \_ su \_ \_ \_ Fase \_ II di backup di ad TPM**</dt> <dt>0x00010000</dt> </dl>   | È in corso la seconda parte dello spazio di archiviazione delle informazioni di autorizzazione del proprietario del TPM in Active Directory.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Informazioni \_ su \_Configurazione legacy**</dt> <dt>0x00020000</dt> </dl>            | Windows Criteri di gruppo è configurato in modo da non archiviare alcuna autorizzazione del proprietario del TPM, quindi il TPM non può essere completamente pronto.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Informazioni \_ su 0x00040000 \_ certificato EK**</dt> <dt></dt> </dl>                              | Il certificato EK non è stato letto dalla RAM TPM NV e archiviato nel registro di sistema. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Informazioni \_ su \_ \_ Registro eventi TCG**</dt> <dt>0x00080000</dt> </dl>                                | Il registro eventi TCG è vuoto o non può essere letto. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Informazioni \_ su 0x00100000 non \_ ridotto**</dt> <dt></dt> </dl>                                       | Il TPM non è di proprietà.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Informazioni \_ su \_Errore generico**</dt> <dt>0x00200000</dt> </dl>                                 | Si è verificato un errore, ma non specifico di un'attività specifica.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Informazioni \_ su \_ \_ Contatore del blocco del dispositivo**</dt> <dt>0x00400000</dt> </dl>              | Il contatore di blocco del dispositivo non è stato creato.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
