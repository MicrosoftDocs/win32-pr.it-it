---
description: Usa il file di certificato fornito per ottenere la chiave derivata e sbloccare il volume crittografato.
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
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317685"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithCertificateFile della \_ classe EncryptableVolume Win32

Il metodo **UnlockWithCertificateFile** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa il file di [*certificato*](../secgloss/c-gly.md) fornito per ottenere la chiave derivata e sbloccare il volume crittografato.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il percorso e il nome del file con estensione cer utilizzato per recuperare l'identificazione personale del certificato. Un certificato di [*crittografia*](../secgloss/e-gly.md) deve essere esportato in formato cer ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) binario con codifica [*x. 509*](../secgloss/x-gly.md) o con codifica base-64 x. 509). Il certificato di crittografia può essere generato da Microsoft PKI, PKI di terze parti o autofirmato.

</dd> <dt>

*Aggiungi* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa di identificazione personale specificata dall'utente. Questa stringa deve essere composta da una sequenza di 4 a 20 cifre. Questa stringa viene usata per autenticare automaticamente il [*provider di archiviazione chiavi*](../secgloss/k-gly.md) (KSP) se usato con una [*Smart Card*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**Errore \_ Il \_ file \_ non**</dt> è stato trovato <dt>0000000002 (0x2)</dt> </dl>                 | Il sistema non è in grado di archiviare il file specificato.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Il volume non può essere sbloccato con le informazioni fornite. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ Autenticazione di E \_ PRIVATEKEY \_ \_ non riuscita**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Non è stato possibile autorizzare la [*chiave privata*](../secgloss/p-gly.md)associata al certificato specificato. L'autorizzazione della chiave privata non è stata specificata o l'autorizzazione fornita non è valida.<br/> |



 

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

 

 
