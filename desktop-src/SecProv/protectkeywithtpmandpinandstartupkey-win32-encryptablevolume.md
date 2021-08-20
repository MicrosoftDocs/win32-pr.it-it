---
description: Protegge la chiave di crittografia del volume usando il Trusted Platform Module (TPM) nel computer, se disponibile, migliorato sia da un PIN specificato dall'utente che da una chiave esterna che deve essere presentata al computer all'avvio.
ms.assetid: 8991c22c-1e36-415e-a82b-c5ddf9c3b24a
title: Metodo ProtectKeyWithTPMAndPINAndStartupKey della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPINAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c4a77c0e5687319bbea438127ce9c30b27ff3122f42359237df5d4cd158b1393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004349"
---
# <a name="protectkeywithtpmandpinandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithTPMAndPINAndStartupKey della classe \_ EncryptableVolume Win32

Il metodo **ProtectKeyWithTPMAndPINAndStartupKey** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume usando il Trusted Platform Module (TPM) nel computer, se disponibile, migliorato sia da un PIN specificato dall'utente che da una chiave esterna che deve essere presentata al computer all'avvio.

Per sbloccare il contenuto crittografato del volume sono necessari tre fattori di autenticazione:

1.  Convalida da parte del TPM
2.  Input di un PIN da 4 a 20 cifre o, se è abilitato il criterio di gruppo "Consenti PIN migliorati per l'avvio", da 4 a 20 lettere, simboli, spazi o numeri
3.  Input di un dispositivo di memoria USB che contiene la chiave esterna

Usare il [**metodo SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) per salvare questa chiave esterna in un file in un dispositivo di memoria USB per l'utilizzo come chiave di avvio. Questo metodo si applica solo al volume del sistema operativo. Viene creata una protezione con chiave di tipo "TPM, PIN e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithTPMAndPINAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile,
  [in]           string PIN,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che etichetta questa protezione con chiave. Se questo parametro non viene specificato, viene usato un valore vuoto.

</dd> <dt>

*PlatformValidationProfile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8**

Matrice di numeri interi che specifica il modo in cui il TPM del computer protegge la chiave di crittografia del volume. Un profilo di convalida della piattaforma è costituito da un set di indici PCR (Platform Configuration Register) compresi tra 0 e 23 inclusi. I valori di ripetizione nel parametro vengono ignorati. Ogni indice PCR è associato ai servizi eseguiti all'avvio del sistema operativo. Ogni volta che il computer viene avviato, il TPM verifica che i servizi specificati nel profilo di convalida della piattaforma non sono stati modificati. Se uno di questi servizi cambia mentre la protezione BitLocker rimane attiva, il TPM non rilascerà la chiave di crittografia per sbloccare il volume e il computer verrà attivato in modalità di ripristino.

Se questo parametro non viene specificato, vengono usati gli indici predefiniti 0, 2, 4, 5, 8, 9, 10 e 11. Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia dalle modifiche apportate a Core Root of Trust of Measurement (CRTM), BIOS e Platform Extensions (PCR 0), Option ROM Code (PCR 2), MBR (Master Boot Record) Code (PCR 4), MBR (Master Boot Record) Partition Table (PCR 5), NTFS Boot Sector (PCR 8), NTFS Boot Block (PCR 9),  Boot Manager (PCR 10) e Controllo di accesso BitLocker (PCR 11). Per impostazione Extensible Firmware Interface computer basati su UEFI (Unified Extensible Firmware Interface) non usano PCR 5.

È consigliabile il profilo di convalida della piattaforma predefinito. Per una protezione aggiuntiva dalle modifiche della configurazione di avvio anticipato, usare un profilo di PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica del profilo predefinito influisce sulla sicurezza e sulla gestibilità del computer. La sensibilità di BitLocker alle modifiche della piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda rispettivamente dell'inclusione o dell'esclusione delle regole di criteri di protezione dei dati. Per abilitare la protezione BitLocker, il profilo di convalida della piattaforma deve includere PCR 11.



| Valore                                                                         | Significato                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Radice principale di attendibilità delle misurazioni (CRTM), BIOS ed estensioni della piattaforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configurazione e dati della piattaforma e della scheda madre<br/>                         |
| <dl> <dt>2</dt> </dl>  | Codice ROM dell'opzione<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configurazione e dati dell'opzione ROM<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Codice MBR (Master Boot Record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabella delle partizioni MBR (Master Boot Record)<br/>                                |
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

Tipo: **string**

Contiene un PIN da 4 a 20 cifre oppure, se è abilitato il criterio di gruppo "Consenti PIN migliorati per l'avvio", 4 e 20 lettere, simboli, spazi o numeri. Questa stringa deve essere fornita al computer all'avvio.

</dd> <dt>

*Chiave esterna* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave esterna a 256 bit utilizzata per sbloccare il volume all'avvio del computer. Lasciare vuoto questo parametro per generare in modo casuale la chiave esterna. Usare il [**metodo GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) per ottenere la chiave generata in modo casuale.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco aggiornato usato per gestire una protezione con chiave del volume crittografata.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | Viene fornito il parametro *PlatformValidationProfile,* ma i relativi valori non sono all'interno dell'intervallo noto o non corrispondono all'impostazione Criteri di gruppo corrente.<br/> Il *parametro ExternalKey* viene fornito ma non è una matrice di dimensioni 32.<br/> |
| <dl> <dt>**FVE \_ E \_ BOOTABLE \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | In questo computer è disponibile un CD/DVD di avvio. Rimuovere il CD/DVD e riavviare il computer.<br/>                                                                                                                                                                               |
| <dl> <dt>**FVE \_ E \_ VOLUME \_ 2150694947**</dt> <dt>(0x80310023)</dt> </dl>              | Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.<br/>                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ CARATTERI \_ PIN \_ NON**</dt> <dt>VALIDI 2150695066 (0x8031009A)</dt> </dl>          | Il *parametro NewPIN* contiene caratteri non validi. Quando l'opzione "Consenti PIN migliorati per l'Criteri di gruppo" è disabilitata, sono supportati solo i numeri.<br/>                                                                                                        |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | Il volume è bloccato.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ POLICY INVALID PIN LENGTH \_ \_ \_ 2150695016**</dt> <dt>(0x80310068)</dt> </dl> | Il *parametro NewPIN* specificato è più lungo di 20 caratteri, più breve di 4 caratteri o più breve della lunghezza minima specificata da Criteri di gruppo.<br/>                                                                                                          |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS 2150694961**</dt> <dt>(0x80310031)</dt> </dl>            | Esiste già una protezione con chiave di questo tipo.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl>        | Non è stato trovato alcun TPM compatibile in questo computer.<br/>                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Commenti

Al massimo può esistere una protezione con chiave di tipo "TPM e PIN e chiave di avvio" per un volume in qualsiasi momento. Se si vuole modificare il nome visualizzato o il profilo di convalida della piattaforma usato da una protezione con chiave "TPM e PIN e chiave di avvio" esistente, è necessario prima rimuovere la protezione della chiave esistente e quindi chiamare **ProtectKeyWithTPMAndPINAndStartupKey** per crearne una nuova.

È necessario specificare altre protezione delle chiavi per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio quando il TPM non è in grado di eseguire correttamente la convalida rispetto al profilo di convalida della piattaforma o quando il PIN viene perso. Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più chiavi di protezione per il ripristino di un volume altrimenti bloccato.

Sebbene sia possibile avere una protezione con chiave di tipo "TPM" e un'altra di tipo "TPM e PIN e chiave di avvio", la presenza del tipo di protezione della chiave "TPM" nega gli effetti di altre protezione delle chiavi basate su TPM.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise con SP1, Windows Vista Ultimate solo con app desktop SP1 \[\]<br/>     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
