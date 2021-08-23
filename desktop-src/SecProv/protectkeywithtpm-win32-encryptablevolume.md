---
description: Se il Trusted Platform Module (TPM) è disponibile, questo metodo protegge la chiave di crittografia del volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Metodo ProtectKeyWithTPM della Win32_EncryptableVolume classe
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
ms.openlocfilehash: f7e9c2c424ea84436292158753de29294bbce3a5516b5ab0a9149892640963ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667171"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithTPM della classe \_ EncryptableVolume Win32

Il **metodo ProtectKeyWithTPM** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protegge la chiave di crittografia del volume usando l'hardware di sicurezza Trusted Platform Module (TPM), se disponibile.

Viene creata una protezione con chiave di tipo "TPM" per il volume, se non ne esiste già una.

Questo metodo è applicabile solo al volume che contiene il sistema operativo attualmente in esecuzione e se non esiste già una protezione con chiave nel volume.

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

Tipo: **string**

Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione con chiave. Se questo parametro non viene specificato, viene usato un valore vuoto.

</dd> <dt>

*PlatformValidationProfile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di numeri interi che specifica il modo in cui l'hardware di sicurezza TPM (Trusted Platform Module) del computer protegge la chiave di crittografia del volume del disco.

Un profilo di convalida della piattaforma è costituito da un set di indici PCR (Platform Configuration Register) compresi tra 0 e 23 inclusi. I valori di ripetizione nel parametro vengono ignorati. Ogni indice PCR è associato ai servizi eseguiti all'avvio del sistema operativo. Ogni volta che il computer viene avviato, il TPM verifica che i servizi specificati nel profilo di convalida della piattaforma non sono stati modificati. Se uno di questi servizi cambia mentre la protezione Crittografia unità BitLocker (BDE) rimane attiva, il TPM non rilascerà la chiave di crittografia per sbloccare il volume del disco e il computer entrarà in modalità di ripristino.

Se questo parametro viene specificato mentre l'impostazione Criteri di gruppo è stata abilitata, deve corrispondere all Criteri di gruppo predefinita.

Se questo parametro non viene specificato, viene usato il valore predefinito 0, 2, 4, 5, 8, 9, 10 e 11. Il profilo di convalida della piattaforma predefinito protegge la chiave di crittografia dalle modifiche apportate a Core Root of Trust of Measurement (CRTM), BIOS e Platform Extensions (PCR 0), Option ROM Code (PCR 2), MBR (Master Boot Record) Code (PCR 4), MBR (Master Boot Record) Partition Table (PCR 5), NTFS Boot Sector (PCR 8), NTFS Boot Code (PCR 9),  Boot Manager (PCR 10) e Crittografia unità BitLocker Access Control (PCR 11). Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per impostazione Extensible Firmware Interface computer basati su UEFI (Unified Extensible Firmware Interface) non usano PCR 5. Per una protezione aggiuntiva dalle modifiche della configurazione di avvio anticipato, usare un profilo di PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica del profilo predefinito influisce sulla sicurezza e sulla gestibilità del computer. La sensibilità di BitLocker alle modifiche della piattaforma (dannose o autorizzate) viene aumentata o ridotta a seconda rispettivamente dell'inclusione o dell'esclusione delle regole di criteri di protezione dei dati. Per abilitare la protezione BitLocker, il profilo di convalida della piattaforma deve includere PCR 11.



| Valore                                                                         | Significato                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Radice principale di attendibilità delle misurazioni (CRTM), BIOS ed estensioni della piattaforma.<br/> |
| <dl> <dt>1</dt> </dl>  | Configurazione e dati della piattaforma e della scheda madre<br/>                          |
| <dl> <dt>2</dt> </dl>  | Codice ROM dell'opzione<br/>                                                          |
| <dl> <dt>3</dt> </dl>  | Configurazione e dati dell'opzione ROM<br/>                                        |
| <dl> <dt>4</dt> </dl>  | Codice MBR (Master Boot Record)<br/>                                            |
| <dl> <dt>5</dt> </dl>  | Tabella delle partizioni MBR (Master Boot Record)<br/>                                 |
| <dl> <dt>6</dt> </dl>  | Eventi di transizione e riattivazione dello stato<br/>                                         |
| <dl> <dt>7</dt> </dl>  | Computer Manufacturer-Specific<br/>                                           |
| <dl> <dt>8</dt> </dl>  | Settore di avvio NTFS<br/>                                                         |
| <dl> <dt>9</dt> </dl>  | Codice di avvio NTFS<br/>                                                           |
| <dl> <dt>10</dt> </dl> | Boot Manager<br/>                                                             |
| <dl> <dt>11</dt> </dl> | Crittografia unità BitLocker controllo di accesso<br/>                                |
| <dl> <dt>12</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                           |
| <dl> <dt>13</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                           |
| <dl> <dt>14</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                           |
| <dl> <dt>15</dt> </dl> | Definito per l'uso da parte del sistema operativo statico<br/>                           |
| <dl> <dt>16</dt> </dl> | Usato per il debug<br/>                                                       |
| <dl> <dt>17</dt> </dl> | CRTM dinamico<br/>                                                             |
| <dl> <dt>18</dt> </dl> | Piattaforma definita<br/>                                                         |
| <dl> <dt>19</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                         |
| <dl> <dt>20</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                         |
| <dl> <dt>21</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                         |
| <dl> <dt>22</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                         |
| <dl> <dt>23</dt> </dl> | Supporto delle applicazioni<br/>                                                      |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Stringa che identifica in modo univoco la protezione creata e che può essere usata per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl>        | Il volume è bloccato.<br/>                                                                                                                                                   |
| <dl> <dt>**TB \_ E \_ SERVIZIO \_ NON \_ IN**</dt> <dt>ESECUZIONE 2150121480 (0x80284008)</dt> </dl> | Non è stato trovato alcun TPM compatibile in questo computer.<br/>                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ FOREIGN \_ VOLUME**</dt> <dt>2150694947 (0x80310023)</dt> </dl>       | Il TPM non è in grado di proteggere la chiave di crittografia del volume perché il volume non contiene il sistema operativo attualmente in esecuzione.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | Il *parametro PlatformValidationProfile* viene fornito ma i relativi valori non sono nell'intervallo noto o non corrispondono all'impostazione Criteri di gruppo corrente.<br/> |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ EXISTS 2150694961**</dt> <dt>(0x80310031)</dt> </dl>            | Esiste già una protezione con chiave di questo tipo.<br/>                                                                                                                             |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Per la sicurezza del computer, è consigliabile usare il profilo predefinito. Per una protezione aggiuntiva dalle modifiche della configurazione di avvio anticipato, usare un profilo di PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

La modifica del profilo predefinito influisce sulla sicurezza o sull'usabilità del computer.

## <a name="remarks"></a>Commenti

Per un volume può esistere al massimo una protezione con chiave di tipo "TPM" in qualsiasi momento. Se si vuole modificare il nome visualizzato o il profilo di convalida della piattaforma usato da una protezione con chiave "TPM" esistente, è necessario prima rimuovere la protezione con chiave esistente e quindi chiamare **ProtectKeyWithTPM** per crearne una nuova.

Per gli indici PCR da 0 a 5, le misurazioni correnti nei registri vengono usate per proteggere la chiave di crittografia. Per i valori PCR da 8 a 11, le misurazioni usate sono quelle previste per il ciclo di avvio successivo.

È necessario specificare protezione con chiave aggiuntiva per sbloccare il volume negli scenari di ripristino in cui non è possibile ottenere l'accesso alla chiave di crittografia del volume. ad esempio quando il TPM non è in grado di eseguire correttamente la convalida rispetto al profilo di convalida della piattaforma. Usare [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) o [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) per creare una o più protezione con chiave per il ripristino di un volume altrimenti bloccato.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
