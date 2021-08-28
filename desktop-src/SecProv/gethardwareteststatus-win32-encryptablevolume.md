---
description: Fornisce informazioni sullo stato di un test hardware di un volume del sistema operativo completamente decrittografato.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Metodo GetHardwareTestStatus della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 32d0d477459dbc7352d1d8f6779c5c76cfbd537d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475357"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetHardwareTestStatus della classe \_ EncryptableVolume Win32

Il **metodo GetHardwareTestStatus** della classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) fornisce informazioni sullo stato di un test hardware di un volume del sistema operativo completamente decrittografato.

Usare questo metodo per indicare se un test hardware è in sospeso, nonché l'esito positivo o negativo di un test hardware completato all'ultimo riavvio del computer. Per richiedere un test hardware, usare [**il metodo EncryptAfterHardwareTest.**](encryptafterhardwaretest-win32-encryptablevolume.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato test* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Specifica se un test hardware è in sospeso, nonché l'esito positivo di un test hardware completato all'ultimo riavvio del computer.




| valore | Significato | 
|-------|---------|
| <span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl><dt><strong>NotFailed_and_NonePending</strong></dt><dt>0</dt></dl> | Se è stato richiesto un test, il test ha avuto esito positivo all'ultimo riavvio del computer e la crittografia del volume è in corso. Per lo stato della crittografia, vedere il <a href="getconversionstatus-win32-encryptablevolume.md"><strong>metodo GetConversionStatus.</strong></a> In caso contrario, non è stato eseguito alcun test all'ultimo riavvio del computer e nessuno è in sospeso. <br /> | 
| <span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl><dt><strong>Errore</strong></dt><dt>1</dt></dl> | La crittografia del volume non è stata avviata. Tutte le protezione con chiave sono state rimosse.<br /> Per risolvere un test non superato:<br /><ul><li>Consultare le informazioni nel <em>parametro TestError.</em></li><li>Aggiungere le protezione con chiave e usare <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>di nuovo il metodo EncryptAfterHardwareTest.</strong></a></li></ul> | 
| <span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl><dt><strong>In sospeso</strong></dt><dt>2</dt></dl> | È stato richiesto un test che verrà eseguito al successivo riavvio del computer.<br /> | 




 

</dd> <dt>

*TestError* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Specifica l'errore dell'ultimo test hardware completato.



| valore                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Non si sono verificati errori o non è stato eseguito alcun test hardware all'ultimo riavvio del computer.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | FVE \_ E \_ KEYFILE NON \_ \_ TROVATO<br/> Non è stata trovata un'unità flash USB con un file di chiave esterna. Se l'errore persiste, il computer non può leggere le unità USB durante il riavvio. Potrebbe non essere possibile usare chiavi esterne per sbloccare il volume del sistema operativo durante il riavvio.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E \_ KEYFILE \_ INVALID<br/> Il file di chiave esterna nell'unità flash USB è danneggiato. Provare un'altra unità flash USB per archiviare il file di chiave esterna.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ DISABILITATO<br/> Il TPM è disabilitato o disattivato oppure è disabilitato e disattivato. Per attivare il TPM, usare il provider WMI [**\_ Win32 Tpm**](win32-tpm.md) o eseguire lo snap-in di gestione TPM (Tpm.msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | FVE \_ E \_ TPM \_ INVALID \_ PCR<br/> Il TPM ha rilevato una modifica nei servizi di riavvio del sistema operativo all'interno del profilo di convalida della piattaforma corrente. Rimuovere qualsiasi CD o DVD di avvio dal computer. Se l'errore persiste, verificare che siano installati gli aggiornamenti più recenti del firmware e del BIOS e che il TPM funzioni correttamente.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | PIN FVE \_ E \_ NON \_ VALIDO<br/> Il PIN specificato non è corretto.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Nella tabella seguente sono elencati alcuni codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è riuscito.<br/> |
| <dl> <dt>**FVE \_ E \_ BLOCCATO \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/> |



 

## <a name="remarks"></a>Commenti

Per richiedere un test hardware, usare [**il metodo EncryptAfterHardwareTest.**](encryptafterhardwaretest-win32-encryptablevolume.md)

Per eseguire un test hardware quando lo stato è in sospeso, seguire questa procedura:

1.  Inserire nel computer un'unità flash USB che contiene un file di chiave esterna. Questo passaggio si applica solo se il volume ha una protezione con chiave di tipo "Chiave esterna" o "TPM e chiave di avvio".
2.  Riavviare il computer. Al riavvio del computer, il test hardware viene eseguito automaticamente.

Per annullare il test dell'hardware, usare il [**metodo Encrypt.**](encrypt-win32-encryptablevolume.md)

Un test riuscito determina che:

-   Il TPM può sbloccare il volume se esiste una protezione con chiave correlata al TPM.
-   Il computer può leggere un'unità flash USB che contiene un file di chiave esterna durante l'avvio se il volume può essere sbloccato da una chiave esterna (inclusa una chiave di avvio).

I risultati dei test hardware non saranno disponibili dopo eventuali modifiche nella conversione o dopo il successivo riavvio del computer. Controllare nel registro eventi di sistema le informazioni relative ai test hardware eseguiti in precedenza nel computer.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
