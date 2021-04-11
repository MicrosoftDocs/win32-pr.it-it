---
description: Il metodo IsEndorsementKeyPairPresent della \_ classe TPM Win32 indica se la coppia di chiavi di verifica dell'autenticità esiste nel dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Metodo IsEndorsementKeyPairPresent della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131987"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Metodo IsEndorsementKeyPairPresent della \_ classe TPM Win32

Il metodo **IsEndorsementKeyPairPresent** della classe [**\_ TPM Win32**](win32-tpm.md) indica se la coppia di chiavi di verifica dell'autenticità esiste nel dispositivo. La coppia di chiavi di verifica dell'autenticità è obbligatoria prima che il dispositivo possa essere proprietario. Questa coppia di chiavi può essere creata dal metodo [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .

Il dispositivo deve essere abilitato e attivato affinché questo metodo abbia esito positivo. Per abilitare e attivare un dispositivo senza proprietario, vedere il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ out\]
</dt> <dd>

Tipo: **booleano**

Se true, la coppia di chiavi di **Verifica dell'autenticità** esiste nel dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
