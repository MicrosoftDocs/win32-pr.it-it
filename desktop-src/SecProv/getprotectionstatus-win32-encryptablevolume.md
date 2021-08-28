---
description: Indica se il volume e la relativa chiave di crittografia sono protetti.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Metodo GetProtectionStatus della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 66fcbcfc4c5f228fde786a6b9d8913cc69c0d341
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471507"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetProtectionStatus della classe \_ EncryptableVolume Win32

Il **metodo GetProtectionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il volume e la relativa chiave di crittografia (se presente) sono protetti.

La protezione è disattivata se un volume non è crittografato o parzialmente crittografato o se la chiave di crittografia del volume è disponibile in chiaro sul disco rigido.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtectionStatus* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Specifica se il volume e la chiave di crittografia (se presenti) sono protetti.




| valore | Significato | 
|-------|---------|
| <span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl><dt><strong>Non protetto</strong></dt><dt>0</dt></dl> | PROTEZIONE DISATTIVATA<br /> Per un hdd standard:<br /> Il volume è non crittografato, parzialmente crittografato o la chiave di crittografia del volume è disponibile in chiaro sul disco rigido. La chiave di crittografia è disponibile in chiaro sul disco rigido se le protezione con chiave sono state disabilitate usando il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o se non è stata specificata alcuna protezione con chiave usando i metodi seguenti:<ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> Per un EHDD:<br /> La banda per il volume viene sbloccata per sempre, non ha un gestore delle chiavi o è gestita da un gestore delle chiavi di terze parti.<br /> Ciò può anche significare che la banda è gestita da BitLocker, ma è stato chiamato il <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>metodo DisableKeyProtectors</strong></a> e l'unità è sospesa.<br /> | 
| <span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl><dt><strong>Protetto</strong></dt><dt>1</dt></dl> | PROTEZIONE ON<br /> Per un hdd standard:<br /> Il volume è completamente crittografato e la chiave di crittografia per il volume non è disponibile in chiaro sul disco rigido.<br /> Per un EHDD:<br /> BitLocker è il gestore delle chiavi per la banda. L'unità può essere bloccata o sbloccata, ma non può essere sbloccata in modo perpetuo.<br /> | 
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl><dt><strong>Sconosciuto</strong></dt><dt>2</dt></dl> | Non è possibile determinare lo stato di protezione del volume. Ciò può essere causato dal fatto che il volume è in stato bloccato.<br /><strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Questo valore non è supportato. Questo valore è supportato a partire da Windows 7 e Windows Server 2008 R2.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile crittografare un volume solo se si [**chiama prima DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) o si usa uno dei metodi seguenti:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Pertanto, se il disco è crittografato e *ProtectionStatus* restituisce zero (PROTECTION OFF), le chiavi vengono disabilitate.

Usare [**GetKeyProtectors per**](getkeyprotectors-win32-encryptablevolume.md) elencare le protezione con chiave specificate per proteggere la chiave di crittografia del volume. Se esistono protezioni con chiave ma la protezione è zero (PROTECTION OFF), usare [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) per attivare la protezione del volume.

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

 

 
