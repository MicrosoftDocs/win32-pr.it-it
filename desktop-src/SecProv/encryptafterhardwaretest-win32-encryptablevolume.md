---
description: Avvia la crittografia di un volume del sistema operativo completamente decrittografato dopo un test hardware.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Metodo EncryptAfterHardwareTest della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5365bd9aca023d42d9f2ab1d9de5d242497b8b21842004b2bb508f362752bd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004499"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a>Metodo EncryptAfterHardwareTest della classe \_ EncryptableVolume Win32

Il **metodo EncryptAfterHardwareTest** della [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) avvia la crittografia di un volume del sistema operativo completamente decrittografato dopo un test hardware. Per eseguire questo test hardware è necessario un riavvio. Usare questo metodo anziché il [**metodo Encrypt**](encrypt-win32-encryptablevolume.md) per verificare che BitLocker funzioni come previsto.

> [!Note]  
> Se il disco rigido è crittografato con hardware, questo metodo non crittografa i dati. Imposta invece lo stato della banda su sbloccato da "sbloccato in modo perpetuo". Se la banda è bloccata, sbloccata o di sola lettura, l'unità viene considerata crittografata.

 

## <a name="syntax"></a>Sintassi


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptionMethod* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint32**

Specifica l'algoritmo di crittografia e le dimensioni della chiave usati per crittografare il volume. Lasciare vuoto questo parametro per usare il valore predefinito zero. Se il volume è parzialmente o completamente crittografato, il valore di questo parametro deve essere 0 o corrispondere al metodo di crittografia esistente del volume. Se l'impostazione Criteri di gruppo è stata abilitata con un valore valido, il valore di questo parametro deve essere 0 o corrispondere all'Criteri di gruppo predefinita.

Se l'impostazione Criteri di gruppo non è valida, viene usato il valore predefinito AES 128 con diffusore.



| Valore                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <dt>**Non specificato**</dt> <dt>0</dt> </dl> | Usare l'impostazione Criteri di gruppo, se disponibile e valida, oppure il metodo di crittografia predefinito in caso contrario.<br/>                                                                              |
| <dl> <dt>1</dt> </dl>                                                                                                                                                                | AES 128 CON DIFFUSORE<br/> Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello diffusore e usando una dimensione della chiave AES di 128 bit.<br/> |
| <dl> <dt>2</dt> </dl>                                                                                                                                                                | AES 256 CON DIFFUSORE<br/> Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) migliorato con un livello diffusore e usando una dimensione della chiave AES di 256 bit.<br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <dt>**AES \_ 128**</dt> <dt>3</dt> </dl>                                          | Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) e usando una dimensione della chiave AES di 128 bit.<br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <dt>**AES \_ 256**</dt> <dt>4</dt> </dl>                                          | Crittografare il volume usando l'algoritmo Advanced Encryption Standard (AES) e usando una dimensione della chiave AES di 256 bit.<br/>                                                                 |



 

</dd> <dt>

*Flag di crittografia* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint32**

Flag che descrivono il comportamento di crittografia.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise e Windows Server 2008:** Questo parametro non è disponibile.

Combinazione di 32 bit con i bit seguenti attualmente definiti.



| Valore                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Eseguire la crittografia dei volumi in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia. Se la crittografia è stata sospesa o arrestata, la chiamata al metodo [**Encrypt**](encrypt-win32-encryptablevolume.md) riprende in modo efficace la conversione e il valore di questo bit viene ignorato. Questo bit ha effetto solo quando i metodi **Encrypt** o **EncryptAfterHardwareTest** avviano la crittografia dallo stato completamente decrittografato, dalla decrittografia in corso o dallo stato di sospensione della decrittografia. Se questo bit è zero, ovvero non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Eseguire la cancellazione su richiesta dello spazio disponibile del volume. La chiamata [**al metodo Encrypt**](encrypt-win32-encryptablevolume.md) con questo bit impostato è consentita solo quando il volume non è attualmente in fase di conversione o di pulizia e si trova in uno stato "crittografato".<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>0x00010000 </dt> </dl> | Eseguire l'operazione richiesta in modo sincrono. La chiamata verrà interrotta fino al completamento o all'interruzione dell'operazione richiesta. Questo flag è supportato solo con il [**metodo Encrypt.**](encrypt-win32-encryptablevolume.md) Questo flag può essere specificato quando **viene chiamato Encrypt** per riprendere la crittografia o l'interruzione della crittografia o della pulizia oppure quando è in corso la crittografia o la pulizia. Ciò consente al chiamante di riprendere in modo sincrono l'attesa fino al completamento o all'interruzione del processo.<br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Questo metodo restituisce immediatamente . Se il volume è già completamente crittografato e non vengono restituiti altri errori, questo metodo restituisce zero.



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
<td>Il <em>parametro EncryptionMethod</em> viene fornito ma non è compreso nell'intervallo noto o non corrisponde all'impostazione Criteri di gruppo corrente.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </dl></td>
<td>Non esiste alcuna chiave di crittografia per il volume.<br/> Disabilitare le protezione delle chiavi usando il <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>metodo DisableKeyProtectors</strong></a> oppure usare uno dei metodi seguenti per specificare le protezione delle chiavi per il volume:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </dl></td>
<td>Impossibile crittografare il volume perché questo computer è configurato per far parte di un cluster di server.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </dl></td>
<td>Non sono disponibili protezione con chiave di tipo TPM, TPM e PIN, TPM e PIN e chiave di &quot; &quot; &quot; &quot; &quot; &quot; avvio, &quot; TPM &quot; &quot; e &quot; chiave di avvio o Chiave esterna. Il test dell'hardware riguarda solo le chiavi di protezione precedenti.<br/> Se si vuole comunque eseguire un test hardware, è necessario usare uno dei metodi seguenti per specificare le chiavi di protezione per il volume:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </dl></td>
<td>Il volume è parzialmente o completamente crittografato.<br/> Il test dell'hardware si applica prima che venga eseguita la crittografia. Se si vuole comunque eseguire il test, usare prima il metodo <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> e quindi uno dei metodi seguenti per aggiungere le chiavi di protezione:
<ul>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </dl></td>
<td>Il volume è un volume di dati.<br/> Il test hardware si applica solo ai volumi che possono avviare il sistema operativo. Eseguire questo metodo nel volume del sistema operativo attualmente avviato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </dl></td>
<td>Non sono specificate chiavi di protezione &quot; di tipo Password &quot; numerica. Il Criteri di gruppo richiede un backup delle informazioni di ripristino per Active Directory Domain Services. Per aggiungere almeno una protezione con chiave di quel tipo, usare il <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>metodo ProtectKeyWithNumericalPassword.</strong></a><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Quando si usa questo metodo senza il secondo parametro facoltativo (in base alla definizione Windows 7 e Windows Vista Enterprise), il metodo avvierà sempre la conversione in modalità completa per mantenere il comportamento compatibile con le versioni precedenti. In questo modo l'aspettativa di sicurezza delle applicazioni e degli script esistenti non verrà interrotta con l'aggiunta del secondo parametro facoltativo in Windows 8 e Windows Server 2012.

A differenza [**del metodo Encrypt,**](encrypt-win32-encryptablevolume.md) questo metodo esegue le operazioni seguenti:

-   Verifica se il TPM sarà in grado di sbloccare il volume, se esiste una protezione con chiave correlata al TPM.
-   Verifica se il computer può leggere un'unità flash USB che contiene un file di chiave esterna durante l'avvio, se il volume verrà sbloccato da una chiave esterna (inclusa una chiave di avvio).
-   Richiede un riavvio del computer per eseguire il test dell'hardware.
-   Avvia la crittografia solo se il test dell'hardware ha esito positivo.
-   Non può essere usato in un volume di dati, in un volume parzialmente o completamente crittografato o per riprendere la crittografia.

Prima di eseguire questo metodo, usare i metodi seguenti per creare le relative chiavi di protezione:

-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Dopo aver eseguito questo metodo, seguire questa procedura aggiuntiva:

1.  Inserire nel computer un'unità flash USB contenente un file di chiave esterna. Questo passaggio si applica solo se il volume ha una protezione con chiave di tipo "Chiave esterna" o "TPM e chiave di avvio".
2.  Riavviare il computer.

Al riavvio del computer, il test hardware viene eseguito automaticamente.

La crittografia inizia se il test dell'hardware ha esito positivo. In caso contrario, provare a risolvere eventuali errori hardware. Eseguire [**GetHardwareTestStatus dopo**](gethardwareteststatus-win32-encryptablevolume.md) il riavvio del computer per ottenere i risultati dei test.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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
</dt> </dl>

 

 
