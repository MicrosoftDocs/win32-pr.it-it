---
description: Enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Metodo FindValidCertificates della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347256"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Metodo FindValidCertificates della \_ classe EncryptableVolume Win32

Il metodo **FindValidCertificates** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali. L'elenco restituito contiene solo certificati con un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) valido. L'OID può essere il valore predefinito oppure può essere specificato nella Criteri di gruppo.

## <a name="syntax"></a>Sintassi


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertificateThumbprint* \[ out\]
</dt> <dd>

Tipo: **stringa \[ \]**

Matrice di stringhe che contiene l'elenco di certificati validi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                           | Descrizione                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Il metodo è stato eseguito correttamente.<br/>                |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> non valido </dl> | L'OID di BitLocker disponibile non è valido.<br/> |



 

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

 

 
