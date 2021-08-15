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
ms.openlocfilehash: da642ff24fa01d27c74a30af7de6c7f91e33a712a28c47644a7044f43c40d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892439"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Metodo FindValidCertificates della classe \_ EncryptableVolume Win32

Il **metodo FindValidCertificates** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) enumera tutti i certificati nel sistema che corrispondono ai criteri indicati e restituisce un elenco di identificazioni personali. L'elenco restituito contiene solo certificati con un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) valido. L'OID può essere l'impostazione predefinita o può essere specificato nel Criteri di gruppo.

## <a name="syntax"></a>Sintassi


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertificateThumbprint* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] string**

Matrice di stringhe che contiene l'elenco di certificati validi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                           | Descrizione                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | Il metodo è stato eseguito correttamente.<br/>                |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID BITLOCKER non valido**</dt> 2150695022 <dt>(0x8031006E)</dt> </dl> | L'OID di BitLocker disponibile non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise, Windows solo app desktop Ultimate 7 \[\]<br/>                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
