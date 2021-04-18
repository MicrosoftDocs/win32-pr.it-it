---
description: Convalida l'identificatore di oggetto (EKU) di utilizzo chiavi avanzato (OID) del certificato fornito.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Metodo ProtectKeyWithCertificateThumbprint della classe Win32_EncryptableVolume
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
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315337"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Metodo ProtectKeyWithCertificateThumbprint della \_ classe EncryptableVolume Win32

Il metodo **ProtectKeyWithCertificateThumbprint** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) convalida l' [*identificatore di oggetto*](../secgloss/o-gly.md) (EKU) dell'utilizzo chiavi avanzato (EKU) del certificato fornito.

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

Tipo: **stringa**

Stringa che specifica un identificatore di stringa assegnato dall'utente per la protezione con chiave. Se questo parametro non viene specificato, il parametro *FriendlyName* viene creato usando il nome del soggetto nel certificato.

</dd> <dt>

*CertThumbprint* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica l'identificazione digitale del certificato.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **stringa**

Stringa che identifica in modo univoco la protezione con chiave creata che può essere utilizzata per gestire la protezione con chiave.

Se l'unità supporta la crittografia hardware e BitLocker non ha assunto la proprietà della banda, la stringa ID è impostata su "BitLocker" e la protezione con chiave viene scritta in base ai metadati della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**Errore \_ \_Data 13 non valida**</dt> <dt>(0xD)</dt> </dl>                                           | I dati non sono validi.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ non \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | L'attributo EKU del certificato specificato non consente di utilizzarlo per Crittografia unità BitLocker. BitLocker non richiede che un certificato disponga di un attributo EKU, ma se ne è stato configurato uno, deve essere impostato su un OID che corrisponda all'OID configurato per BitLocker.<br/> |
| <dl> <dt>**FVE \_ Il \_ certificato utente del criterio E \_ \_ non è \_ \_ consentito**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Criteri di gruppo non consente l'utilizzo di certificati utente, ad esempio smart card, con BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ Il \_ certificato utente del criterio E \_ \_ \_ deve \_ essere \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Per Criteri di gruppo è necessario fornire una smart card per l'utilizzo di BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ Il \_ criterio E \_ impedisce a \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Criteri di gruppo non consente l'uso di certificati autofirmati.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Se l'OID non corrisponde a quello associato al controller del servizio nel registro di sistema, questo metodo ha esito negativo. In questo modo si impedisce all'utente di impostare manualmente i programmi di protezione dell'agente di recupero dati (DRA) nel volume. DRAs devono essere impostati solo dal servizio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
