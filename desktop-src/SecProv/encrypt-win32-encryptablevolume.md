---
description: Avvia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato.
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
ms.openlocfilehash: 968ff7f64a9a98a711210a4cfae64006c5a8f965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481027"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a>Metodo Encrypt della classe \_ EncryptableVolume Win32

Il **metodo Encrypt** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) avvia la crittografia di un volume completamente decrittografato o riprende la crittografia di un volume parzialmente crittografato. Quando la crittografia è sospesa o in corso, questo metodo si comporta come [**ResumeConversion.**](resumeconversion-win32-encryptablevolume.md) Quando la decrittografia viene sospesa o in corso, questo metodo arresta la decrittografia e avvia la crittografia.

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

Tipo: **uint32**

Intero senza segno che specifica l'algoritmo di crittografia e le dimensioni della chiave utilizzate per crittografare il volume. Se questo parametro è maggiore di zero e il volume è parzialmente o completamente crittografato, *EncryptionMethod* deve corrispondere al metodo di crittografia esistente del volume. Se questo parametro è maggiore di zero e l'impostazione Criteri di gruppo è abilitata con un valore valido, *EncryptionMethod* deve corrispondere all'Criteri di gruppo predefinita.

Per un elenco dei possibili valori EncryptionMethod, vedere il [**metodo GetEncryptionMethod.**](getencryptionmethod-win32-encryptablevolume.md)

Il valore predefinito per Windows 7 o inferiore è: 1 (AES \_ 128 \_ WITH \_ DIFFUSER).

Il valore predefinito per Windows 8, Windows 8.1 o Windows 10 versione 1507 è: 3 (AES \_ 128).

Il valore predefinito per Windows 10 versione 1511 o successiva è: 6 (XTS \_ AES \_ 128).

</dd> <dt>

*Flag di crittografia* \[ in, facoltativo\]
</dt> <dd>

Tipo: **uint32**

Flag che descrivono il comportamento di crittografia.

**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise e Windows Server 2008:** Questo parametro non è disponibile.

Combinazione di 32 bit con i bit seguenti attualmente definiti.



| valore                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl>  | Eseguire la crittografia dei volumi in modalità di crittografia solo dati all'avvio di un nuovo processo di crittografia. Se la crittografia è stata sospesa o arrestata, la chiamata al metodo **Encrypt** riprende in modo efficace la conversione e il valore di questo bit viene ignorato. Questo bit ha effetto solo quando i metodi **Encrypt** o [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) avviano la crittografia dallo stato completamente decrittografato, dalla decrittografia in corso o dallo stato di sospensione della decrittografia. Se questo bit è zero, ovvero non è impostato, quando si avvia un nuovo processo di crittografia, verrà eseguita la conversione in modalità completa.<br/> |
| <dl> <dt>0x00000002</dt> </dl>  | Eseguire la cancellazione su richiesta dello spazio disponibile del volume. La chiamata **al metodo Encrypt** con questo bit impostato è consentita solo quando il volume non è attualmente in fase di conversione o di pulizia e si trova in uno stato "crittografato".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>0x00010000 </dt> </dl> | Eseguire l'operazione richiesta in modo sincrono. La chiamata verrà interrotta fino al completamento o all'interruzione dell'operazione richiesta. Questo flag è supportato solo con il **metodo Encrypt.** Questo flag può essere specificato quando **viene chiamato Encrypt** per riprendere la crittografia o l'interruzione della crittografia o della pulizia oppure quando è in corso la crittografia o la pulizia. Ciò consente al chiamante di riprendere in modo sincrono l'attesa fino al completamento o all'interruzione del processo.<br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Questo metodo restituisce immediatamente . Se il volume è già completamente crittografato e non vengono restituiti altri errori, questo metodo restituisce 0.




| Codice/valore restituito | Descrizione | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Il metodo è stato eseguito correttamente.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt><dt>2147942487 (0x80070057)</dt></dl> | Il <em>parametro EncryptionMethod</em> viene fornito ma non è compreso nell'intervallo noto o non corrisponde all'impostazione Criteri di gruppo corrente.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt><dt>2150694958 (0x8031002E)</dt></dl> | Non esiste alcuna chiave di crittografia per il volume. Disabilitare le protezione delle chiavi usando il <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>metodo DisableKeyProtectors</strong></a> oppure usare uno dei metodi seguenti per specificare le protezione delle chiavi per il volume:<br /><ul><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><strong>Windows Vista:</strong> Quando non esiste alcuna chiave di crittografia per il volume, ERROR_INVALID_OPERATION viene restituita. Il valore decimale è 4317 e il valore esadecimale è 0x10DD.<br /> | 
| <dl><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt><dt>2150694957 (0x8031002D)</dt></dl> | Il metodo di crittografia fornito non corrisponde a quello del volume parzialmente o completamente crittografato. Per continuare la crittografia, lasciare vuoto <em>il parametro EncryptionMethod</em> o usare un valore pari a zero.<br /> | 
| <dl><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt><dt>2150694942 (0x8031001E)</dt></dl> | Impossibile crittografare il volume perché questo computer è configurato per far parte di un cluster di server.<br /> | 
| <dl><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt><dt>2150694912 (0x80310000)</dt></dl> | Il volume è bloccato.<br /> | 
| <dl><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt><dt>2150694956 (0x8031002C)</dt></dl> | Non sono specificate chiavi di protezione di tipo "Password numerica". Il Criteri di gruppo richiede un backup delle informazioni di ripristino per Active Directory Domain Services. Per aggiungere almeno una protezione con chiave di quel tipo, usare il <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>metodo ProtectKeyWithNumericalPassword.</strong></a><br /> | 




 

## <a name="remarks"></a>Commenti

Quando si usa questo metodo senza il secondo parametro facoltativo (in base alla definizione Windows 7 e Windows Vista Enterprise), il metodo avvierà sempre la conversione in modalità completa per mantenere il comportamento compatibile con le versioni precedenti. In questo modo l'aspettativa di sicurezza delle applicazioni e degli script esistenti non verrà interrotta con l'aggiunta del secondo parametro facoltativo in Windows 8 e Windows Server 2012.

È possibile chiamare [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) per determinare se la crittografia è in corso e la percentuale del volume crittografato.

Dopo che il volume è completamente crittografato e se le protezioni con chiave sono state aggiunte e abilitate, lo stato di protezione per il volume cambia in "attivato".

Managed Object Format (MOF) contengono le definizioni per le Windows wmi (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
