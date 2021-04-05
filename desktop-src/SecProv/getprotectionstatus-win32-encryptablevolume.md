---
description: Indica se il volume e la relativa chiave di crittografia sono protetti.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Metodo GetProtectionStatus della classe Win32_EncryptableVolume
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
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750842"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Metodo GetProtectionStatus della \_ classe EncryptableVolume Win32

Il metodo **GetProtectionStatus** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se il volume e la relativa chiave di crittografia (se presenti) sono protetti.

La protezione è disattivata se un volume non è crittografato o parzialmente crittografato o se la chiave di crittografia del volume è disponibile in chiaro sul disco rigido.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtectionStatus* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Specifica se il volume e la chiave di crittografia (se presenti) sono protetti.



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
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <dt><strong></strong></dt> <dt>0</dt> non protetto </dl></td>
<td>PROTEZIONE NON ATTIVA<br/> Per un HDD standard:<br/> Il volume non è crittografato, parzialmente crittografato o la chiave di crittografia del volume è disponibile in chiaro sul disco rigido. La chiave di crittografia è disponibile in chiaro sul disco rigido se le protezioni con chiave sono state disabilitate tramite il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> o se non sono state specificate protezioni con chiave utilizzando i metodi seguenti:
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/> Per un EHDD:<br/> La banda per il volume viene continuamente sbloccata, non ha un gestore chiavi o è gestita da un gestore di chiavi di terze parti.<br/> Questo può anche significare che la banda è gestita da BitLocker, ma il metodo <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> è stato chiamato e l'unità viene sospesa.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Protetto</strong></dt> <dt>1</dt> </dl></td>
<td>PROTEZIONE SU<br/> Per un HDD standard:<br/> Il volume è completamente crittografato e la chiave di crittografia per il volume non è disponibile in chiaro sul disco rigido.<br/> Per un EHDD:<br/> BitLocker è il gestore chiavi della banda. L'unità può essere bloccata o sbloccata, ma non può essere sbloccata continuamente.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Sconosciuto</strong></dt> <dt>2</dt> </dl></td>
<td>Impossibile determinare lo stato di protezione del volume. Questo problema può essere causato dal fatto che il volume si trova in uno stato bloccato.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Questo valore non è supportato. Questo valore è supportato a partire da Windows 7 e Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile crittografare un volume solo se si chiama prima [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) o si usa uno dei metodi seguenti:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Se pertanto il disco è crittografato e *ProtectionStatus* restituisce zero (Protection off), le chiavi vengono disabilitate.

Usare [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) per elencare le protezioni con chiave che sono state specificate per proteggere la chiave di crittografia del volume. Se esistono protezioni con chiave ma la protezione è zero (protezione disattivata), usare [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) per attivare la protezione del volume.

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

 

 
