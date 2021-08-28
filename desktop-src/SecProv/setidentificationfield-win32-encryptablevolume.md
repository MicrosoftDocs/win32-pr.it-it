---
description: Imposta la stringa dell'identificatore specificata nei metadati del volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Metodo SetIdentificationField della Win32_EncryptableVolume classe
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
ms.openlocfilehash: 473b10bda95177fa2019a7439b46b475ac3bb8477ef45e19d945e8a7c1bc87a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004269"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Metodo SetIdentificationField della classe \_ EncryptableVolume Win32

Il **metodo SetIdentificationField** della [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) imposta la stringa dell'identificatore specificata nei metadati del volume.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Campo di identificazione* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che specifica il campo di identificazione assegnato al volume. Se la stringa facoltativa non è presente, vengono usati i valori del set del Registro di sistema. Se la stringa è presente e non vuota, viene usato il valore specificato. Il *parametro IdentificationField* non fa distinzione tra maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ BLOCCO \_ DEL VOLUME**</dt> 2150694912 <dt>(0x80310000)</dt> </dl> | Questa unità è bloccata da Crittografia unità BitLocker. È necessario sbloccare questo volume da Pannello di controllo. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker. <br/>                    |



 

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

 

 




