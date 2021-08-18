---
description: Il metodo IsSrkAuthCompatible della classe Win32 Tpm indica se l'autorizzazione Archiviazione Root Key (SRK) è compatibile con il valore previsto \_ da Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Metodo IsSrkAuthCompatible della Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 435829389749d7f7e81552aa88dd00aa211fd74ae079c93c97b5baff3c7a3c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891853"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a>Metodo IsSrkAuthCompatible della classe \_ Win32 Tpm

Il metodo **IsSrkAuthCompatible** della classe [**\_ Win32 Tpm**](win32-tpm.md) indica se l'autorizzazione Archiviazione Root Key (SRK) è compatibile con il valore previsto da Windows Vista.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsSrkAuthCompatible* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** il valore di autorizzazione SRK ha un valore pari a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
