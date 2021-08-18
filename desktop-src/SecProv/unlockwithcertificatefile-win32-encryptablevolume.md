---
description: Usa il file del certificato fornito per ottenere la chiave derivata e sbloccare il volume crittografato.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Metodo UnlockWithCertificateFile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004229"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithCertificateFile della classe \_ EncryptableVolume Win32

Il **metodo UnlockWithCertificateFile** della [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa il [*file*](../secgloss/c-gly.md) di certificato fornito per ottenere la chiave derivata e sbloccare il volume crittografato.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato".

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa che specifica il percorso e il nome del file cer usato per recuperare l'identificazione personale del certificato. Un [*certificato*](../secgloss/e-gly.md) di crittografia deve essere esportato in formato [*CER*](../secgloss/d-gly.md) ( Distinguished Encoding Rules (DER) [*binario X.509*](../secgloss/x-gly.md) o X.509 con codifica Base 64. Il certificato di crittografia può essere generato da microsoft PKI, PKI di terze parti o autofirmato.

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
| <dl> <dt>**ERRORE \_ FILE \_ NON \_ TROVATO 0000000002**</dt> <dt>(0x2)</dt> </dl>                 | Il sistema non è in grado di salvare il file specificato.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ FAILED \_ AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Non è possibile sbloccare il volume con le informazioni fornite. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ E \_ PROTEZIONE NON TROVATA \_ \_ 2150694963**</dt> <dt>(0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | La [*chiave privata,*](../secgloss/p-gly.md)associata al certificato specificato, non può essere autorizzata. L'autorizzazione della chiave privata non è stata fornita o l'autorizzazione specificata non è valida.<br/> |



 

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

 

 
