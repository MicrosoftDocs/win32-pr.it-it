---
description: Usa l'identificazione personale del certificato fornita per ottenere la chiave derivata e sbloccare il volume crittografato.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Metodo UnlockWithCertificateThumbprint della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0ccf4a68f999bee1d32d8025759eb9625371b18fc5028b54e68e62df544bbd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891366"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithCertificateThumbprint della classe \_ EncryptableVolume Win32

Il **metodo UnlockWithCertificateThumbprint** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa l'identificazione personale del certificato fornita per ottenere la chiave derivata e sbloccare il volume crittografato. [](../secgloss/c-gly.md)

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertThumbprint* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Viene accettato un valore di identificazione personale pari a 0 e viene restituita una ricerca del certificato appropriato nell'archivio locale. Se viene trovato un singolo certificato di BitLocker, la ricerca ha esito positivo. Se non viene trovato nessuno o più certificati, il metodo ha esito negativo.

</dd> <dt>

*PIN* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa di identificazione personale specificata dall'utente. Questa stringa deve essere costituita da una sequenza da 4 a 20 cifre. Questa stringa viene usata per autenticare automaticamente il provider di [*archiviazione chiavi*](../secgloss/k-gly.md) (KSP) quando viene usato con un [*smart card*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Non è possibile sbloccare il volume usando le informazioni fornite. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ PROTEZIONE NON TROVATA \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Non [*è stato possibile*](../secgloss/p-gly.md) autorizzazionere la chiave privata associata al certificato specificato. L'autorizzazione della chiave privata non è stata fornita o l'autorizzazione specificata non è valida.<br/> |



 

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

 

 
