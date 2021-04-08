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
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750826"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Metodo UnlockWithCertificateThumbprint della \_ classe EncryptableVolume Win32

Il metodo **UnlockWithCertificateThumbprint** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) usa l'identificazione personale del [*certificato*](../secgloss/c-gly.md) fornita per ottenere la chiave derivata e sbloccare il volume crittografato.

> [!Note]  
> Se il disco supporta la crittografia hardware, questa funzione imposta lo stato della banda su "sbloccato" "

 

## <a name="syntax"></a>Sintassi


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CertThumbprint* \[ in\]
</dt> <dd>

Tipo: **stringa**

Viene accettato un valore di identificazione personale pari a 0, che comporta la ricerca dell'archivio locale per il certificato appropriato. Se viene trovato un singolo certificato BitLocker, la ricerca ha esito positivo. Se non viene trovato nessuno o più di un certificato, il metodo ha esito negativo.

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
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ \_ autenticazione non riuscita**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | Non è possibile sbloccare il volume utilizzando le informazioni fornite. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ \_Protezione E \_ non \_ trovata**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | La protezione con chiave specificata non esiste nel volume. È necessario immettere un'altra protezione con chiave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ Autenticazione di E \_ PRIVATEKEY \_ \_ non riuscita**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | Non è stato possibile autorizzare la [*chiave privata*](../secgloss/p-gly.md) associata al certificato specificato. L'autorizzazione della chiave privata non è stata specificata o l'autorizzazione fornita non è valida.<br/> |



 

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

 

 
