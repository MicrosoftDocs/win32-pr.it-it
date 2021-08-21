---
description: "Metodo ProtectKeyWithCertificateFile della classe Win32_EncryptableVolume : convalida l'identificatore di oggetto EKU (Enhanced Key Usage) del certificato fornito."
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Metodo ProtectKeyWithCertificateFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e96667af5e9c16097e951f3162082a6fb06b13d0504da3e8582b9f1b7ebfd4cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004459"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithCertificateFile della classe \_ EncryptableVolume Win32

Il **metodo ProtectKeyWithCertificateFile** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) convalida l'identificatore di oggetto EKU [*(Enhanced*](../secgloss/o-gly.md) Key Usage) del certificato fornito.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione della chiave. Se questo parametro non viene specificato, il *parametro FriendlyName* viene creato usando il nome soggetto nel certificato.

</dd> <dt>

*FileName* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il percorso e il nome del file cer usato per abilitare BitLocker. Un certificato di crittografia deve essere esportato in formato con estensione cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) binario con codifica [*X.509*](../secgloss/x-gly.md) o Con codifica Base 64 X.509. Il certificato di crittografia può essere generato da Microsoft PKI, PKI di terze parti o autofirmato.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica in modo univoco la protezione delle chiavi creata che può essere usata per gestire la protezione delle chiavi.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione della chiave viene scritta in per ogni metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se non riesce.



| Codice/valore restituito                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | L'attributo EKU del certificato specificato non ne consente l'uso per Crittografia unità BitLocker. BitLocker non richiede che un certificato abbia un attributo EKU, ma se ne è configurato uno, deve essere impostato su un OID corrispondente all'OID configurato per BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ CERTIFICATO UTENTE CRITERI \_ \_ \_ NON \_**</dt> CONSENTITO 2150695026 <dt>(0x80310072)</dt> </dl> | Criteri di gruppo non consente l'uso di certificati utente, ad esempio smart card, con BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ USER \_ CERT MUST BE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Criteri di gruppo è necessario specificare un smart card usare BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Criteri di gruppo non consente l'uso di certificati autofirmati.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRORE \_ FILE \_ NON \_ TROVATO 0000000002**</dt> <dt>(0x2)</dt> </dl>                                | Impossibile trovare il file specificato.<br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Se l'OID non corrisponde a quello associato al controller del servizio nel Registro di sistema, questo metodo ha esito negativo. Ciò impedisce all'utente di impostare manualmente le protezione dell'agente di recupero dati (DRA) nel volume. I contratti di ripristino di emergenza devono essere impostati solo dal servizio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows 7 app desktop Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
