---
description: Disabilita il provisioning automatico del TPM se è attualmente abilitato.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D Metodo isableAutoProvisioning
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
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314669"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a>\_TPM Win32::D Metodo isableautoprovisioning

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

Se impostato su **true**, il provisioning automatico è disabilitato solo per l'avvio successivo. Se è impostato su **false** o non è specificato, il provisioning automatico è disabilitato in modo permanente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
