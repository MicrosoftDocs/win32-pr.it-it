---
description: Indica se il provisioning automatico del TPM è abilitato.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: Win32_Tpm::IsAutoProvisioningEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 53541922b803a7898b66ce363a5718114b6c5f6d3913a6cde86650200ae76770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890856"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a>Metodo Win32 \_ Tpm::IsAutoProvisioningEnabled

Indica se il provisioning automatico del TPM è abilitato. Per impostazione predefinita, il provisioning automatico è abilitato per Windows 8 e Windows Server 2012.

Questo metodo è accessibile solo dagli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsAutoProvisioningEnabled* \[ Cambio\]
</dt> <dd>

Impostare su **TRUE se** il provisioning automatico TPM è abilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori TPM e gli errori specifici dei [servizi di base TPM.](../tbs/tbs-return-codes.md)

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ Radice \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
