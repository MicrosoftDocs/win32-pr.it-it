---
description: Disabilita il provisioning automatico del TPM se è attualmente abilitato.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 910695cc599445e6df027c0eed3ba8aa5575ad0166e06ef167d6c3ccc049c135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004129"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a>Metodo \_ Win32 Tpm::D isableAutoProvisioning

Disabilita il provisioning automatico del TPM se è attualmente abilitato. L'operazione non ha alcun effetto se il provisioning automatico è già disabilitato. Per impostazione predefinita, il provisioning automatico è abilitato per Windows 8 e Windows Server 2012.

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OnlyForNextBoot* \[ in, facoltativo\]
</dt> <dd>

Se impostato su **TRUE,** il provisioning automatico è disabilitato solo per l'avvio successivo. Se impostato su **FALSE o** non specificato, il provisioning automatico viene disabilitato in modo permanente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi [di base TPM.](../tbs/tbs-return-codes.md)

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
