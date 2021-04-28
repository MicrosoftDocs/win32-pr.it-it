---
description: "Metodo ProtectKeyWithCertificateThumbprint della classe Win32_EncryptableVolume: convalida l'identificatore di oggetto (OID) di utilizzo chiavi avanzato (EKU) del certificato fornito."
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Metodo ProtectKeyWithCertificateThumbprint della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110579"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithCertificateThumbprint della classe \_ EncryptableVolume Win32

Il **metodo ProtectKeyWithCertificateThumbprint** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) convalida l'identificatore di oggetto (OID) [](../secgloss/o-gly.md) di Utilizzo chiavi avanzato (EKU) del certificato fornito.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che specifica un identificatore di stringa assegnato dall'utente per questa protezione con chiave. Se questo parametro non viene specificato, il *parametro FriendlyName* viene creato usando il nome soggetto nel certificato.

</dd> <dt>

*CertThumbprint* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa che specifica l'identificazione personale del certificato.

</dd> <dt>

*VolumeKeyProtectorID* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Stringa che identifica in modo univoco la protezione con chiave creata che può essere usata per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID viene impostata su "BitLocker" e la protezione con chiave viene scritta per metadati di banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**ERRORE \_ DATI \_ NON**</dt> <dt>VALIDI 13 (0xD)</dt> </dl>                                           | I dati non sono validi.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | L'attributo EKU del certificato specificato non ne consente l'uso per Crittografia unità BitLocker. BitLocker non richiede che un certificato abbia un attributo EKU, ma se ne è configurato uno, deve essere impostato su un OID corrispondente all'OID configurato per BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ CERTIFICATO UTENTE CRITERI NON \_ \_ \_ \_ CONSENTITO**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Criteri di gruppo non consente l'uso di certificati utente, ad esempio smart card, con BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY \_ USER \_ CERT DEVE ESSERE \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Criteri di gruppo è necessario specificare un smart card usare BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY \_ PROHIBITS \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Criteri di gruppo non consente l'uso di certificati autofirmati.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Se l'OID non corrisponde a quello associato al controller del servizio nel Registro di sistema, questo metodo ha esito negativo. Ciò impedisce all'utente di impostare manualmente le protezione dell'agente di recupero dati (DRA) nel volume. I contratti di ripristino di emergenza devono essere impostati solo dal servizio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
