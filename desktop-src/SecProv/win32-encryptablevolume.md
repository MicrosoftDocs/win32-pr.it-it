---
description: Per la crittografia delle unità o per creare software di sicurezza della crittografia, è possibile usare il software di crittografia Windows, Crittografia unità BitLocker, un'API di crittografia che è possibile usare tramite la classe \_ del provider WMI EncryptableVolume Win32.
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3beb3498cf9e3d2873ea7dcfe3a108618eeddb513bc8207d1e819cce2fe976d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891004"
---
# <a name="win32_encryptablevolume-class"></a>Classe \_ EncryptableVolume Win32

La classe del provider WMI **Win32 \_ EncryptableVolume** rappresenta un'area di archiviazione su un disco rigido che può essere protetta tramite Crittografia unità BitLocker. È possibile crittografare solo i volumi NTFS. Può essere un volume che contiene un sistema operativo o un volume di dati nel disco locale. Non può essere un'unità di rete.

Per ottenere i vantaggi di BitLocker, è necessario specificare un metodo di protezione per la chiave di crittografia del volume e quindi crittografare completamente il volume.

Per proteggere la chiave di crittografia del volume, aggiungere le protezione con chiave usando questi metodi:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Ogni tipo di protezione con chiave offre un'esperienza di autenticazione diversa per sbloccare l'accesso ai dati crittografati. Le chiavi esterne e le password numeriche possono fornire l'autenticazione durante gli scenari di ripristino. Per le protezione con chiave basata su TPM, potrebbe essere prima necessario inizializzare correttamente il TPM. Per altre informazioni, vedere la classe del provider WMI [**\_ Win32 Tpm.**](win32-tpm.md)

Usare il [**metodo Encrypt**](encrypt-win32-encryptablevolume.md) o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) per iniziare la crittografia. Le protezione con chiave devono essere aggiunte prima di avviare la crittografia. In caso contrario, è necessario usare il metodo [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) per esporre una chiave non crittografata non protetta. Se il computer si spegne mentre è in corso la crittografia, la crittografia verrà ripresa automaticamente al riavvio del computer.

È possibile usare i [**metodi GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) [**e GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) per controllare lo stato di un volume accessibile.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>Members

La **classe \_ EncryptableVolume Win32** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ EncryptableVolume Win32** include questi metodi.



| Metodo                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Salva tutte le chiavi esterne e le informazioni correlate necessarie per il ripristino in Active Directory.<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Modifica la chiave esterna associata a un volume crittografato.<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Usa la nuova passphrase per ottenere una nuova chiave derivata.<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | Modifica un PIN associato a un volume crittografato.<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Rimuove tutte le chiavi esterne e le informazioni correlate salvate nel volume del sistema operativo attualmente in esecuzione usate per sbloccare automaticamente i volumi di dati.<br/>                                                                                                             |
| [**Decrittografare**](decrypt-win32-encryptablevolume.md)                                                                       | Avvia la decrittografia di un volume completamente crittografato o riprende la decrittografia di un volume parzialmente crittografato.<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Elimina una protezione con chiave specificata per il volume.<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Elimina tutte le protezione con chiave per il volume.<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Rimuove la chiave esterna salvata nel volume del sistema operativo attualmente in esecuzione in modo che il volume non sia sbloccato automaticamente quando viene montato.<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Disabilita tutte le protezione con chiave associate a questo volume.<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Consente lo sblocco automatico di un volume di dati quando il volume viene montato.<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Abilita tutte le protezione con chiave disabilitata.<br/>                                                                                                                                                                                                                                       |
| [**Crittografare**](encrypt-win32-encryptablevolume.md)                                                                       | Avvia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato.<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Avvia la crittografia di un volume completamente decrittografato dopo un test dell'hardware.<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | Enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali.<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Indica lo stato della crittografia o della decrittografia nel volume.<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Indica l'algoritmo di crittografia e le dimensioni della chiave utilizzati nel volume.<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Restituisce il nome del file che contiene la chiave esterna.<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Restituisce la chiave esterna da un file.<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Restituisce informazioni sullo stato di un test hardware.<br/>                                                                                                                                                                                                                             |
| [**GetIdentificationField**](getidentificationfield-win32-encryptablevolume.md)                                         | Restituisce la stringa dell'identificatore disponibile nei metadati del volume.<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Restituisce informazioni che consentono di salvare i dati crittografati quando l'unità è danneggiata in modo grave.<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Recupera la chiave pubblica e l'identificazione personale del certificato per una protezione con chiave pubblica.<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Recupera la chiave esterna per una protezione con chiave specificata del tipo appropriato.<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Recupera il nome visualizzato utilizzato per identificare una protezione con chiave specificata.<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Recupera la password numerica per una protezione con chiave specificata del tipo appropriato.<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Recupera il profilo di convalida della piattaforma per una protezione con chiave specificata del tipo appropriato.<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Elenca le protezione usate per proteggere la chiave di crittografia del volume.<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Indica il tipo di una protezione con chiave specificata.<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Indica se il contenuto del volume è accessibile dal sistema operativo attualmente in esecuzione.<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Indica se il volume e la relativa chiave di crittografia (se presente) sono protetti.<br/>                                                                                                                                                                                                  |
| [**GetVersion**](getversion-win32-encryptablevolume.md)                                                                 | Indica la versione dei metadati FVE del volume.<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | Indica se il volume viene sbloccato automaticamente al momento del montaggio.<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Indica se nel volume del sistema operativo attualmente in esecuzione sono presenti chiavi esterne e informazioni correlate che possono essere usate per sbloccare automaticamente i volumi di dati.<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Indica se sono disponibili protezione per il volume.<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Indica se la password numerica soddisfa i requisiti di formato speciale.<br/>                                                                                                                                                                                            |
| [**Lock**](lock-win32-encryptablevolume.md)                                                                             | Smonta il volume e rimuove la chiave di crittografia del volume dalla memoria di sistema.<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Sospende la crittografia o la decrittografia di un volume.<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | Crea un volume BitLocker con il tipo di file system specificato del volume di individuazione.<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Convalida l'identificatore di oggetto (OID) di Utilizzo chiavi avanzato (EKU) del file del certificato fornito.<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Convalida l'identificatore di oggetto (OID) di Utilizzo chiavi avanzato (EKU) dell'identificazione personale del certificato fornita.<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Protegge la chiave di crittografia del volume con una chiave esterna a 256 bit.<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Protegge la chiave di crittografia del volume con una password di 48 cifre formattata in modo speciale.<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Usa la passphrase per ottenere la chiave derivata.<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Protegge la chiave di crittografia del volume usando l'hardware Trusted Platform Module (TPM) nel computer, se disponibile.<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Protegge la chiave di crittografia del volume usando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da un PIN (Personal Identification Number) specificato dall'utente che deve essere fornito al computer all'avvio.<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Protegge la chiave di crittografia del volume usando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da un PIN specificato dall'utente e da una chiave esterna che deve essere fornita al computer all'avvio.<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Protegge la chiave di crittografia del volume usando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da una chiave esterna che deve essere fornita al computer all'avvio.<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Riprende la crittografia o la decrittografia di un volume.<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Scrive la chiave esterna associata alla protezione con chiave di volume specificata in un percorso di file specificato.<br/>                                                                                                                                                                   |
| [**SetIdentificationField**](setidentificationfield-win32-encryptablevolume.md)                                         | Imposta la stringa dell'identificatore specificata nei metadati del volume.<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Usa il file del certificato fornito per ottenere la chiave derivata e sbloccare il volume crittografato.<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Usa l'identificazione personale del certificato fornita per ottenere la chiave derivata e sbloccare il volume crittografato.<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Usa una chiave esterna fornita per accedere al contenuto di un volume di dati.<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Usa una password numerica fornita per accedere al contenuto di un volume di dati.<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Usa la passphrase per ottenere la chiave derivata. Dopo aver calcolato la chiave derivata, la chiave derivata viene usata per sbloccare la chiave master del volume crittografato.<br/>                                                                                                                   |
| [**Aggiornamentovolume**](upgradevolume-win32-encryptablevolume.md)                                                           | Aggiorna un volume dal formato Windows Vista al formato Windows 7.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ EncryptableVolume** ha queste proprietà.

<dl> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identificatore univoco del volume in questo sistema. Usare questa opzione per associare un volume ad altre classi di provider WMI, ad esempio Volume **Win32 \_**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lettera di unità del volume. Questo identificatore può essere usato per associare un volume ad altre classi di provider WMI, ad esempio [**volume Win32. \_**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))

Per i volumi senza lettere di unità, questo valore è **NULL.**

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore permanente per il volume in questo sistema. Questo identificatore è esclusivo di **Win32 \_ EncryptableVolume.**

Questo identificatore è una stringa vuota se il volume è un volume NTFS completamente decrittografato standard. in caso contrario, ha un valore univoco.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del volume, indipendentemente dal fatto che BitLocker proteggono o meno il volume. Questo valore viene archiviato quando viene creata un'istanza della classe . È possibile che lo stato di protezione cambi tra la creazione di istanze e quando si controlla il valore. Per controllare il valore della **proprietà ProtectionStatus** in tempo reale, usare il [**metodo GetProtectionStatus.**](getprotectionstatus-win32-encryptablevolume.md)



| Valore                                                                        | Significato                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | PROTEZIONE DISATTIVATA<br/> Il volume non è crittografato, parzialmente crittografato o la chiave di crittografia del volume per il volume è disponibile in chiaro sul disco rigido. <br/> |
| <dl> <dt>1</dt> </dl> | PROTEZIONE ON<br/> Il volume è completamente crittografato e la chiave di crittografia per il volume non è disponibile in chiaro sul disco rigido. <br/>                          |
| <dl> <dt>2</dt> </dl> | PROTEZIONE SCONOSCIUTA<br/> Non è possibile determinare lo stato di protezione del volume. Una delle possibili cause è che il volume si trova in uno stato bloccato.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

La classe del provider WMI **Win32 \_ EncryptableVolume** si basa sulla sicurezza dello spazio dei nomi WMI e sul sottosistema Crittografia unità BitLocker per il controllo di accesso.

Per usare i **metodi \_ EncryptableVolume win32,** è necessario che siano soddisfatte le condizioni seguenti:

-   È necessario disporre dei privilegi di amministratore.
-   La crittografia della connessione deve essere in grado di connettersi al provider.

    Per altre informazioni sulla creazione di una connessione crittografata, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi.](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md)

Per abilitare le connessioni remote, è necessario consentire il traffico WMI remoto. Per altre informazioni sull'abilitazione del traffico WMI, vedere [Connessione a WMI in modalità remota a partire da Vista.](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md)

L'impostazione di sicurezza dello spazio dei nomi predefinita include una voce che consente la modifica per impostazione predefinita. Per altre informazioni sul controllo dello spazio dei nomi WMI, vedere [Accesso agli spazi dei nomi WMI.](../wmisdk/access-to-wmi-namespaces.md)

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



 

 
