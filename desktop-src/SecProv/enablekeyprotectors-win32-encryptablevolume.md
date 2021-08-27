---
description: Abilita o riprende tutte le protezione con chiave disabilitata o sospesa.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Metodo EnableKeyProtectors della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474927"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Metodo EnableKeyProtectors della classe \_ EncryptableVolume Win32

Il **metodo EnableKeyProtectors** della classe [**\_ Win32 EncryptableVolume**](win32-encryptablevolume.md) abilita o riprende tutte le protezione con chiave disabilitata o sospesa. È possibile usare questo metodo per riabilita o riprendere la protezione BitLocker in un volume crittografato. Questo metodo garantisce che la chiave di crittografia del volume non sia esposta in chiaro sul disco rigido.

> [!Note]  
> Se il disco supporta la crittografia hardware, lo stato della banda passa a "sbloccato" da "sempre sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.

Se le protezione con chiave sono già abilitate e non si verificano altri errori, questo metodo restituisce zero.




| Codice/valore restituito | Descrizione | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Il metodo è stato eseguito correttamente.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | Nel volume non sono presenti protezione con chiave. Usare uno dei metodi seguenti per specificare le protezione con chiave per il volume:<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br /> | 




 

## <a name="remarks"></a>Commenti

Se il volume è completamente crittografato, l'esecuzione corretta di questo metodo garantisce che il volume sia protetto. Se il volume è parzialmente crittografato, l'esecuzione corretta di questo metodo implica che il volume sarà protetto quando sarà completamente crittografato. Per altre informazioni, vedere il [**metodo GetProtectionStatus.**](getprotectionstatus-win32-encryptablevolume.md)

Se esistono protezione con chiave basata su TPM per il volume, l'esecuzione corretta di questo metodo aggiorna anche queste protezione in modo che il TPM si convalidi rispetto ai servizi di avvio correnti sulla piattaforma. In altre parole, si asserirà che lo stato corrente del computer è lo stato corretto con cui il TPM esegue il controllo in caso di riavvii futuri del computer.

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
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
