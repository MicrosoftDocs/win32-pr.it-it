---
description: Il metodo IsEndorsementKeyPairPresent della classe Win32 Tpm indica se la coppia di chiavi di approvazione \_ esiste nel dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Metodo IsEndorsementKeyPairPresent Win32_Tpm classe
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
ms.openlocfilehash: bcbc0c4877aae2db0e94d42838100720ee0ae0dcbdcc33f52cf70d2e23327e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004469"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Metodo IsEndorsementKeyPairPresent della classe Tpm Win32 \_

Il **metodo IsEndorsementKeyPairPresent** della classe [**\_ Win32 Tpm**](win32-tpm.md) indica se la coppia di chiavi di approvazione esiste nel dispositivo. La coppia di chiavi di approvazione è necessaria prima che il dispositivo possa essere di proprietà. Questa coppia di chiavi può essere creata dal [**metodo CreateEndorsementKeyPair.**](createendorsementkeypair-win32-tpm.md)

Il dispositivo deve essere abilitato e attivato perché questo metodo riesca. Per abilitare e attivare un dispositivo senzawned, vedere il [**metodo SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** la coppia di chiavi di approvazione esiste nel dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
