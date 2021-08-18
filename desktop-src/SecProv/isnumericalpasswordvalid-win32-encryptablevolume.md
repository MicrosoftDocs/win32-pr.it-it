---
description: Indica se la password numerica soddisfa i requisiti di formato speciale per questo valore di autenticazione.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Metodo IsNumericalPasswordValid della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0aed00554d7a8e284f83659dc92266b1ce5e098f1b102e6444bfc07fd2909066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739641"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Metodo IsNumericalPasswordValid della classe \_ EncryptableVolume Win32

Il **metodo IsNumericalPasswordValid** della classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se la password numerica soddisfa i requisiti di formato speciale per questo valore di autenticazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumericalPassword* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Stringa che specifica la password numerica.

La password numerica deve contenere 48 cifre. Queste cifre possono essere suddivise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 720896. Supponendo che un gruppo di sei cifre sia etichettato come x1, x2, x3, x4, x5 e x6, la cifra checksum x6 viene calcolata come –x1+x2-x3+x4-x5 mod 11.

I gruppi di cifre possono facoltativamente essere separati da uno spazio o un trattino. Pertanto, anche "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" o "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere password numeriche valide.

</dd> <dt>

*IsNumericalPasswordValid* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Valore booleano che è true se la password numerica soddisfa i requisiti di formato speciale per questo valore di autenticazione; in caso contrario, il valore è false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/>                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
