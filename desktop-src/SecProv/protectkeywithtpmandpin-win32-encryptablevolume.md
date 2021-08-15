---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume migliorata da un numero di identificazione personale specificato dall'utente.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Metodo ProtectKeyWithTPMAndPIN della Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0eab283a0eaec97d7f7c9e03cf8d8064e08e0e25bea606b393fb35a38143f7fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891406"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithTPMAndPIN della classe \_ EncryptableVolume Win32

Il metodo **ProtectKeyWithTPMAndPIN** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume usando l'hardware di sicurezza Trusted Platform Module (TPM) nel computer, se disponibile, migliorato da un PIN (Personal Identification Number) specificato dall'utente che deve essere fornito al computer all'avvio.

Sia la convalida da parte del TPM che l'input della stringa di identificazione personale sono necessari per accedere alla chiave di crittografia del volume e sbloccare il contenuto del volume.

Questo metodo è applicabile solo per il volume che contiene il sistema operativo attualmente in esecuzione.

Per il volume viene creata una protezione con chiave di tipo "TPM e PIN", se non ne esiste già una.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa assegnato dall'utente per questa protezione della chiave. Se questo parametro non viene specificato, viene usato un valore vuoto.

</dd> <dt>

*PlatformValidationProfile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di interi che specifica il modo in cui l'hardware di sicurezza Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.

Un profilo di convalida della piattaforma è costituito da un set di indici PCR (Platform Configuration Register) compresi tra 0 e 23, inclusi. I valori di ripetizione nel parametro vengono ignorati. Ogni indice PCR è associato ai servizi eseguiti all'avvio del sistema operativo. Ogni volta che il computer viene avviato, il TPM verifica che i servizi specificati nel profilo di convalida della piattaforma non sono stati modificati. Se uno di questi servizi cambia mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascerà la chiave di crittografia per sbloccare il volume del disco e il computer entra in modalità di ripristino.

Se questo parametro viene specificato mentre è stata abilitata l'Criteri di gruppo di configurazione corrispondente, deve corrispondere all'Criteri di gruppo predefinita.

Se questo parametro non viene specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11. Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia dalle modifiche apportate agli elementi seguenti:

-   Radice principale dell'attendibilità delle misurazioni (CRTM)
-   BIOS
-   Estensioni della piattaforma (PCR 0)
-   Codice ROM dell'opzione (PCR 2)
-   Codice MBR (Master Boot Record) (PCR 4)
-   Tabella di partizione MBR (Master Boot Record) (PCR 5)
-   Settore di avvio NTFS (PCR 8)
-   Blocco di avvio NTFS (PCR 9)
-   Boot Manager (PCR 10)
-   Controllo di accesso BitLocker (PCR 11)

Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per una protezione aggiuntiva dalle modifiche di configurazione di avvio anticipato, usare un profilo di PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11. I computer Extensible Firmware Interface basati su UEFI (Unified Extensible Firmware Interface) non usano PCR 5 per impostazione predefinita.

La modifica del profilo predefinito influisce sulla sicurezza e sulla gestibilità del computer. La sensibilità di BitLocker alle modifiche della piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda rispettivamente dell'inclusione o dell'esclusione delle pcr. Per abilitare la protezione BitLocker, il profilo di convalida della piattaforma deve includere PCR 11.



| Valore                                                                         | Significato                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Radice principale dell'attendibilità delle misurazioni (CRTM), BIOS ed estensioni della piattaforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configurazione e dati della piattaforma e della scheda madre<br/>                         |
| <dl> <dt>2</dt> </dl>  | Codice ROM dell'opzione<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Dati e configurazione dell'opzione ROM<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Codice MBR (Master Boot Record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabella di partizione MBR (Master Boot Record)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Eventi di transizione e riattivazione dello stato<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Computer Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Settore di avvio NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Blocco di avvio NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Boot Manager<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Controllo di accesso BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                          |
| <dl> <dt>13</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                          |
| <dl> <dt>14</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                          |
| <dl> <dt>15</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                          |
| <dl> <dt>16</dt> </dl> | Usato per il debug<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinamico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Piattaforma definita<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>23</dt> </dl> | Supporto delle applicazioni<br/>                                                     |



 

</dd> <dt>

*PIN* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa di identificazione personale specificata dall'utente. Questa stringa deve essere costituita da una sequenza di 6-20 cifre o, se è abilitato il criterio di gruppo "Consenti PIN migliorati per l'avvio", da 6 a 20 lettere, simboli, spazi o numeri.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave di volume crittografata.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione della chiave viene scritta in per ogni metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                | Descrizione                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Viene fornito il parametro *PlatformValidationProfile,* ma i relativi valori non sono all'interno dell'intervallo noto o non corrispondono all'impostazione Criteri di gruppo corrente.<br/> |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | In questo computer è disponibile un CD/DVD di avvio. Rimuovere il CD/DVD e riavviare il computer.<br/>                                                                                 |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ 2150694947**</dt> <dt>(0x80310023)</dt> </dl>              | Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.<br/>                                            |
| <dl> <dt>**FVE \_ E \_ CARATTERI \_ PIN \_ NON**</dt> <dt>VALIDI 2150695066 (0x8031009A)</dt> </dl>          | Il *parametro NewPIN* contiene caratteri non validi. Quando l'opzione "Consenti PIN migliorati per l'Criteri di gruppo" è disabilitata, sono supportati solo i numeri.<br/>          |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Il volume è bloccato.<br/>                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ CRITERI LUNGHEZZA PIN \_ \_ \_ NON**</dt> <dt>VALIDA 2150695016 (0x80310068)</dt> </dl> | Il *parametro NewPIN* fornito è più lungo di 20 caratteri, più breve di 6 caratteri o più breve della lunghezza minima specificata da Criteri di gruppo.<br/>            |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS 2150694961**</dt> <dt>(0x80310031)</dt> </dl>            | Esiste già una protezione con chiave di questo tipo.<br/>                                                                                                                             |
| <dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Non è stato trovato alcun TPM compatibile in questo computer.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per una protezione aggiuntiva dalle modifiche del codice di avvio anticipato, usare un profilo di PCR 0, 2, 4, 5, 8, 9, 10 e 11. Per una protezione aggiuntiva dalle modifiche di configurazione di avvio anticipato, usare un profilo di PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica del profilo predefinito influisce sulla sicurezza o sull'usabilità del computer.

## <a name="remarks"></a>Commenti

Al massimo può esistere una protezione con chiave di tipo "TPM e PIN" per un volume in qualsiasi momento. Se si vuole modificare il nome visualizzato o il profilo di convalida della piattaforma usato da una protezione con chiave "TPM e PIN" esistente, è necessario prima rimuovere la protezione della chiave esistente e quindi chiamare **ProtectKeyWithTPMAndPIN** per crearne una nuova.

È necessario specificare altre protezione delle chiavi per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio quando il TPM non è in grado di eseguire correttamente la convalida rispetto al profilo di convalida della piattaforma o quando il PIN viene perso.

Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più chiavi di protezione per il ripristino di un volume altrimenti bloccato.

Sebbene sia possibile avere una protezione con chiave di tipo "TPM" e un'altra di tipo "TPM e PIN", la presenza del tipo di protezione della chiave "TPM" nega gli effetti di altre protezione delle chiavi basate su TPM.

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
</dt> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
