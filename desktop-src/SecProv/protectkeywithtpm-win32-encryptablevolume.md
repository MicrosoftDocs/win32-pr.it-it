---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Metodo ProtectKeyWithTPM della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315335"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithTPM della \_ classe EncryptableVolume Win32

Il metodo **ProtectKeyWithTPM** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume utilizzando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile.

Viene creata una protezione con chiave di tipo "TPM" per il volume, se non ne esiste già una.

Questo metodo è applicabile solo al volume che contiene il sistema operativo attualmente in esecuzione e se una protezione con chiave non esiste già nel volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica un identificatore di stringa assegnato dall'utente per la protezione con chiave. Se questo parametro non è specificato, viene utilizzato un valore blank.

</dd> <dt>

*PlatformValidationProfile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.

Un profilo di convalida della piattaforma è costituito da un set di indici di registro di configurazione della piattaforma (PCR) compresi tra 0 e 23, inclusi. I valori repeat nel parametro vengono ignorati. Ogni indice di PCR è associato ai servizi che vengono eseguiti all'avvio del sistema operativo. Ogni volta che il computer viene avviato, il TPM verificherà che i servizi specificati nel profilo di convalida della piattaforma non siano stati modificati. Se uno di questi servizi viene modificato mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascia la chiave di crittografia per sbloccare il volume del disco e il computer entrerà in modalità di ripristino.

Se questo parametro viene specificato mentre l'impostazione Criteri di gruppo corrispondente è stata abilitata, deve corrispondere all'impostazione Criteri di gruppo.

Se questo parametro non è specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11. Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia in base alle modifiche apportate alla radice principale di Trust of Measurement (CRTM). BIOS, and Platform Extensions (PCR 0), Option ROM code (PCR 2), il codice MBR (master boot record) (PCR 4), la tabella di partizione MBR (master boot record) (PCR 5), il settore di avvio NTFS (PCR 8), il codice di avvio NTFS (PCR 9), Boot Manager (PCR 10) e il controllo di accesso Crittografia unità BitLocker (PCR 11). Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per impostazione predefinita, i computer basati su Unified Extensible Firmware Interface (UEFI) non utilizzano PCR 5. Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica dal profilo predefinito influiscono sulla sicurezza e la gestibilità del computer. La riservatezza delle modifiche da BitLocker a piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda dell'inclusione o dell'esclusione, rispettivamente, del PCRs. Per abilitare la protezione BitLocker, è necessario che il profilo di convalida della piattaforma includa PCR 11.



| Valore                                                                         | Significato                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma.<br/> |
| <dl> <dt>1</dt> </dl>  | Configurazione e dati della piattaforma e della scheda madre<br/>                          |
| <dl> <dt>2</dt> </dl>  | Codice ROM opzione<br/>                                                          |
| <dl> <dt>3</dt> </dl>  | Configurazione e dati dell'opzione ROM<br/>                                        |
| <dl> <dt>4</dt> </dl>  | Codice MBR (master boot record)<br/>                                            |
| <dl> <dt>5</dt> </dl>  | Tabella di partizione MBR (record di avvio principale)<br/>                                 |
| <dl> <dt>6</dt> </dl>  | Eventi di riattivazione e transizione di stato<br/>                                         |
| <dl> <dt>7</dt> </dl>  | Manufacturer-Specific computer<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Settore di avvio NTFS<br/>                                                         |
| <dl> <dt>9</dt> </dl>  | Codice di avvio NTFS<br/>                                                           |
| <dl> <dt>10</dt> </dl> | Gestione avvio<br/>                                                             |
| <dl> <dt>11</dt> </dl> | Controllo di accesso Crittografia unità BitLocker<br/>                                |
| <dl> <dt>12</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                           |
| <dl> <dt>13</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                           |
| <dl> <dt>14</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                           |
| <dl> <dt>15</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                           |
| <dl> <dt>16</dt> </dl> | Usato per il debug<br/>                                                       |
| <dl> <dt>17</dt> </dl> | CRTM dinamico<br/>                                                             |
| <dl> <dt>18</dt> </dl> | Piattaforma definita<br/>                                                         |
| <dl> <dt>19</dt> </dl> | Utilizzato dal sistema operativo attendibile<br/>                                         |
| <dl> <dt>20</dt> </dl> | Utilizzato dal sistema operativo attendibile<br/>                                         |
| <dl> <dt>21</dt> </dl> | Utilizzato dal sistema operativo attendibile<br/>                                         |
| <dl> <dt>22</dt> </dl> | Utilizzato dal sistema operativo attendibile<br/>                                         |
| <dl> <dt>23</dt> </dl> | Supporto delle applicazioni<br/>                                                      |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica in modo univoco la protezione creata e che può essere utilizzata per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl>        | Il volume è bloccato.<br/>                                                                                                                                                   |
| <dl> <dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt> </dl> | Nel computer non è stato trovato alcun TPM compatibile.<br/>                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME esterno**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Il parametro *PlatformValidationProfile* viene specificato, ma i relativi valori non sono compresi nell'intervallo noto o non corrisponde all'impostazione criteri di gruppo attualmente attiva.<br/> |
| <dl> <dt>**FVE \_ La \_ protezione E \_ esiste**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Esiste già una protezione con chiave di questo tipo.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per una protezione aggiuntiva dalle modifiche di configurazione all'avvio iniziale, usare un profilo di PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica dal profilo predefinito influiscono sulla sicurezza o sull'usabilità del computer.

## <a name="remarks"></a>Commenti

Può esistere al massimo una protezione con chiave di tipo "TPM" per un volume in qualsiasi momento. Se si desidera modificare il nome visualizzato o il profilo di convalida della piattaforma utilizzato da una protezione con chiave "TPM" esistente, è necessario prima rimuovere la protezione con chiave esistente e quindi chiamare **ProtectKeyWithTPM** per crearne una nuova.

Per gli indici di PCR da 0 a 5, le misurazioni correnti nei registri vengono usate per proteggere la chiave di crittografia. Per i valori di PCR da 8 a 11, le misurazioni usate sono quelle che dovrebbero esistere al successivo ciclo di avvio.

È necessario specificare protezioni con chiave aggiuntive per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio, quando il TPM non è in grado di convalidare correttamente il profilo di convalida della piattaforma. Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più protezioni con chiave per il ripristino di un volume altrimenti bloccato.

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
</dt> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
