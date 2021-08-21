---
description: Recupera la chiave pubblica e l'identificazione personale del certificato per una protezione con chiave pubblica.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Metodo GetKeyProtectorCertificate della Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e947cb5fadefa6703ab4515ddd8d2a9daf1e7439e514e75c64d3b1e6e885aa0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892064"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorCertificate della classe \_ EncryptableVolume Win32

Il **metodo GetKeyProtectorCertificate** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) [](../secgloss/c-gly.md) recupera la chiave pubblica e l'identificazione personale del certificato per una protezione con chiave pubblica. [](../secgloss/p-gly.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Identificatore di stringa univoco usato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*PublicKey* \[ Cambio\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Matrice di byte che specifica la chiave pubblica.

</dd> <dt>

*CertThumbprint* \[ Cambio\]
</dt> <dd>

Tipo: **string**

Stringa che specifica l'identificazione personale del certificato.

</dd> <dt>

*CertType* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Intero senza segno che specifica il tipo della protezione con chiave. Questo numero intero viene usato per distinguere tra l'agente di recupero dati (DRA) e i certificati utente.



| Valore                                                                        | Significato                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>1</dt> </dl> | Il certificato è un DRA.<br/>     |
| <dl> <dt>2</dt> </dl> | Il certificato non è un DRA.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                                       | Descrizione                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                       | Il metodo è stato eseguito correttamente.<br/>                                                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                               | La protezione con chiave specificata non è una protezione con chiave. È necessario immettere un'altra protezione con chiave.<br/>            |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl>                      | Questa unità è bloccata da Crittografia unità BitLocker. È necessario sbloccare questo volume da Pannello di controllo. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>                      | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                    |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE \_ \_ \_ REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt> </dl> | Criteri di gruppo richiede l'uso di un certificato utente, ad esempio un smart card.<br/>                           |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
