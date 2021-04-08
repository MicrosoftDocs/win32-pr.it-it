---
description: Inizia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Metodo Encrypt della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058224"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Metodo Encrypt della classe Win32 \_ EncryptableVolume

Il metodo **Encrypt** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) inizia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato. Quando la crittografia viene sospesa o in corso, questo metodo si comporta in modo analogo a [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md). Quando la decrittografia è sospesa o in corso, questo metodo interrompe la decrittografia e inizia la crittografia.

> [!Note]  
> Se l'unità è crittografata con hardware, questo metodo non crittografa i dati. Imposta invece lo stato della banda su "sbloccato" da "sempre sbloccato". Se la banda è bloccata, sbloccata o di sola lettura, l'unità viene considerata crittografata.

 

**Windows Vista:** La crittografia di un volume diverso dal volume del sistema operativo attualmente in esecuzione non è supportata.

## <a name="syntax"></a>Sintassi


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptionMethod* \[ in, facoltativo\]
</dt> <dd>

Tipo: **UInt32**

Unsigned Integer che specifica l'algoritmo di crittografia e le dimensioni della chiave usati per crittografare il volume. Se questo parametro è maggiore di zero e il volume è parzialmente o completamente crittografato, *EncryptionMethod* deve corrispondere al metodo di crittografia esistente del volume. Se questo parametro è maggiore di zero e l'impostazione Criteri di gruppo corrispondente è abilitata con un valore valido, *EncryptionMethod* deve corrispondere all'impostazione criteri di gruppo.

Per un elenco dei valori EncryptionMethod possibili, vedere il metodo [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .

Il valore predefinito per Windows 7 o versioni precedenti è: 1 (AES \_ 128 \_ con \_ diffusore).

Il valore predefinito per Windows 8, Windows 8.1 o Windows 10, versione 1507 è: 3 (AES \_ 128).

Il valore predefinito per Windows 10, versione 1511 o successiva è: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*EncryptionFlags* \[ in, facoltativo\]
</dt> <dd>

Tipo: **UInt32**

Flag che descrivono il comportamento di crittografia.

**Windows 7, Windows server 2008 R2, Windows Vista Enterprise e Windows server 2008:** Questo parametro non è disponibile.

Una combinazione di 32 bit con i bit seguenti attualmente definiti.



| Valore                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Eseguire la crittografia del volume in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia. Se la crittografia è stata sospesa o arrestata, la chiamata del metodo **Encrypt** riprende effettivamente la conversione e il valore di questo bit viene ignorato. Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, decrittografia nello stato di avanzamento o decrittografia in pausa. Se questo bit è zero, vale a dire che non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Eseguire la cancellazione su richiesta dello spazio disponibile nel volume. La chiamata al metodo **Encrypt** con questo set di bit è consentita solo quando il volume non è attualmente in fase di conversione o cancellazione e si trova in uno stato "crittografato".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Eseguire in modo sincrono l'operazione richiesta. La chiamata verrà bloccata fino a quando l'operazione richiesta non è stata completata o è stata interrotta. Questo flag è supportato solo con il metodo **Encrypt** . Questo flag può essere **specificato quando viene chiamata la crittografia per** riprendere la crittografia arrestata o interrotta o cancellare o quando è in corso la crittografia o la cancellazione. Ciò consente al chiamante di riprendere l'attesa in modo sincrono finché il processo non viene completato o interrotto.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Questo metodo restituisce immediatamente un risultato. Se il volume è già completamente crittografato e non vengono restituiti altri errori, questo metodo restituisce 0.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice/valore restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </dl></td>
<td>Il metodo è stato eseguito correttamente.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </dl></td>
<td>Il parametro <em>EncryptionMethod</em> è specificato ma non rientra nell'intervallo noto o non corrisponde all'impostazione criteri di gruppo corrente.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Non esiste alcuna chiave di crittografia per il volume. Disabilitare le protezioni con chiave utilizzando il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o utilizzare uno dei metodi seguenti per specificare le protezioni con chiave per il volume:<br/>
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<strong>Windows Vista:</strong> Quando non esiste alcuna chiave di crittografia per il volume, viene invece restituito ERROR_INVALID_OPERATION. Il valore decimale è 4317 e il valore esadecimale è 0x10DD.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </dl></td>
<td>Il metodo di crittografia specificato non corrisponde a quello del volume parzialmente o completamente crittografato. Per continuare la crittografia, lasciare vuoto il parametro <em>EncryptionMethod</em> o usare un valore pari a zero.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Non è possibile crittografare il volume perché questo computer è configurato come parte di un cluster di server.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </dl></td>
<td>Il volume è bloccato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Non è stata specificata alcuna protezione con chiave della &quot; password numerica di tipo &quot; . Per Active Directory Domain Services, il Criteri di gruppo richiede un backup delle informazioni di ripristino. Per aggiungere almeno una protezione con chiave di quel tipo, usare il metodo <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Quando si utilizza questo metodo senza il secondo parametro facoltativo (in base alla definizione di Windows 7 e Windows Vista Enterprise), il metodo avvierà sempre la conversione in modalità completa per mantenere il comportamento compatibile con le versioni precedenti. In questo modo la sicurezza prevista per le applicazioni e gli script esistenti non verrà interruppe con l'aggiunta del secondo parametro facoltativo in Windows 8 e Windows Server 2012.

È possibile chiamare [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) per determinare se la crittografia è in corso e la percentuale del volume crittografato.

Dopo che il volume è stato completamente crittografato e se sono state aggiunte e abilitate le protezioni con chiave, lo stato di protezione del volume viene modificato in "on".

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

 

 
