---
description: Fornisce informazioni sullo stato di un test dell'hardware di un volume del sistema operativo completamente decrittografato.
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
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316111"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetHardwareTestStatus della \_ classe EncryptableVolume Win32

Il metodo **GetHardwareTestStatus** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fornisce informazioni sullo stato di un test hardware di un volume del sistema operativo completamente decrittografato.

Utilizzare questo metodo per indicare se un test hardware è in sospeso, nonché l'esito positivo o negativo di un test hardware completato durante l'ultimo riavvio del computer. Per richiedere un test hardware, usare il metodo [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TestStatus* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Specifica se un test hardware è in sospeso, nonché l'esito negativo di un test hardware completato durante l'ultimo riavvio del computer.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </dl></td>
<td>Se è stato richiesto un test, il test ha avuto esito positivo sull'ultimo riavvio del computer e la crittografia del volume è ora in corso. Per lo stato della crittografia, vedere il metodo <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> . In caso contrario, non viene eseguito alcun test sull'ultimo riavvio del computer e nessuno è in sospeso. <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <dt><strong>Non riuscito</strong></dt> <dt>1</dt> </dl></td>
<td>La crittografia del volume non è stata avviata. Sono state rimosse tutte le protezioni con chiave.<br/> Per risolvere un test non superato:<br/>
<ul>
<li>Consultare le informazioni nel parametro <em>testError</em> .</li>
<li>Aggiungere protezioni con chiave e utilizzare nuovamente il metodo <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <dt><strong>In sospeso</strong></dt> <dt>2</dt> </dl></td>
<td>È stato richiesto un test che verrà eseguito al riavvio successivo del computer.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*TestError* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Specifica l'errore dell'ultimo test hardware completato.



| Valore                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                        | Non si sono verificati errori o non è stato eseguito alcun test hardware nell'ultimo riavvio del computer.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt> 2150694972 (0x8031003C)</dt> </dl> | il \_ file di FVE E non è stato \_ \_ \_ trovato<br/> Non è stata trovata un'unità flash USB con un file di chiave esterna. Se il problema non viene mantenuto, il computer non è in grado di leggere le unità USB durante il riavvio. Potrebbe non essere possibile utilizzare chiavi esterne per sbloccare il volume del sistema operativo durante il riavvio.<br/>                                                                |
| <dl> <dt> 2150694973 (0x8031003D)</dt> </dl> | FVE \_ E il \_ file \_ non è valido<br/> Il file di chiave esterna nell'unità flash USB è danneggiato. Provare con un'altra unità flash USB per archiviare il file di chiave esterna.<br/>                                                                                                                                                                                 |
| <dl> <dt> 2150694975 (0x8031003F)</dt> </dl> | FVE \_ E \_ TPM \_ disabilitato<br/> Il TPM è disabilitato o disattivato o disabilitato e disattivato. Per attivare il TPM, utilizzare il provider [**WMI \_ TPM Win32**](win32-tpm.md) o eseguire lo snap-in Gestione TPM (TPM. msc).<br/>                                                                                                            |
| <dl> <dt> 2150694977 (0x80310041)</dt> </dl> | \_ \_ \_ PCR non valida FVE E TPM \_<br/> Il TPM ha rilevato una modifica nei servizi di riavvio del sistema operativo all'interno del profilo di convalida della piattaforma corrente. Rimuovere qualsiasi CD o DVD di avvio dal computer. Se il problema si verifica in modo permanente, verificare che siano installati gli aggiornamenti più recenti del firmware e del BIOS e che il TPM funzioni correttamente.<br/> |
| <dl> <dt>2150694979 (0x80310043)</dt> </dl>  | FVE \_ E \_ pin \_ non validi<br/> Il PIN specificato non è corretto.<br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è riuscito.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Il volume è bloccato.<br/> |



 

## <a name="remarks"></a>Commenti

Per richiedere un test hardware, usare il metodo [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .

Per eseguire un test hardware quando lo stato è in sospeso, attenersi alla seguente procedura:

1.  Inserire nel computer un'unità flash USB contenente un file di chiave esterna. Questo passaggio si applica solo se il volume ha una protezione con chiave di tipo "chiave esterna" o "TPM e chiave di avvio".
2.  Riavviare il computer. Al riavvio del computer, il test dell'hardware viene eseguito automaticamente.

Per annullare il test dell'hardware, utilizzare il metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) .

Un test con esito positivo determina che:

-   Il TPM può sbloccare il volume se esiste una protezione con chiave TPM correlata.
-   Il computer può leggere un'unità flash USB che contiene un file di chiave esterna durante l'avvio se il volume può essere sbloccato da una chiave esterna (inclusa una chiave di avvio).

I risultati dei test hardware non saranno disponibili dopo le modifiche apportate alla conversione o dopo il riavvio successivo del computer. Controllare nel registro eventi di sistema le informazioni relative a tutti i test hardware eseguiti in precedenza nel computer.

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
</dt> </dl>

 

 
