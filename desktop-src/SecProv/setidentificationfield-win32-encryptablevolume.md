---
description: Imposta la stringa dell'identificatore specificata nei metadati del volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Metodo SetIdentificationField della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884834"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Metodo SetIdentificationField della \_ classe EncryptableVolume Win32

Il metodo **SetIdentificationField** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) imposta la stringa dell'identificatore specificata nei metadati del volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IdentificationField* \[ in, facoltativo\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica il campo di identificazione assegnato al volume. Se la stringa facoltativa non è presente, verranno utilizzati i valori impostati per il registro di sistema. Se la stringa è presente e non è vuota, viene utilizzato il valore specificato. Il parametro *IdentificationField* non fa distinzione tra maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloccato**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Questa unità è bloccata da Crittografia unità BitLocker. È necessario sbloccare questo volume dal pannello di controllo. <br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                    |



 

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

 

 




