---
description: Indica se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione.
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
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315342"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Metodo IsNumericalPasswordValid della \_ classe EncryptableVolume Win32

Il metodo **IsNumericalPasswordValid** della classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) indica se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumericalPassword* \[ in\]
</dt> <dd>

Tipo: **stringa**

Stringa che specifica la password numerica.

La password numerica deve contenere 48 cifre. Queste cifre possono essere divise in 8 gruppi di 6 cifre, con l'ultima cifra in ogni gruppo che indica un valore di checksum per il gruppo. Ogni gruppo di 6 cifre deve essere divisibile per 11 e deve essere minore di 720896. Supponendo che un gruppo di sei cifre sia contrassegnato come X1, X2, X3, X4, X5 e X6, il valore di checksum X6 digit viene calcolato come – X1 + X2 – X3 + X4 – X5 mod 11.

I gruppi di cifre possono essere separati facoltativamente da uno spazio o un trattino. Quindi, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oppure "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" può contenere anche password numeriche valide.

</dd> <dt>

*IsNumericalPasswordValid* \[ out\]
</dt> <dd>

Tipo: **booleano**

Valore booleano che è true se la password numerica soddisfa i requisiti di formato speciali per questo valore di autenticazione; in caso contrario, il valore è false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/>                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
