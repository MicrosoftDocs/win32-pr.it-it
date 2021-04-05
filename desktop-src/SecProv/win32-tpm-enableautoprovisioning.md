---
description: Abilita il provisioning automatico del TPM se è attualmente disabilitato.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Metodo Win32_Tpm:: EnableAutoProvisioning'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343066"
---
# <a name="win32_tpmenableautoprovisioning-method"></a>\_Metodo Win32 TPM:: EnableAutoProvisioning

Abilita il provisioning automatico del TPM se è attualmente disabilitato. L'operazione non ha alcun effetto se il provisioning automatico è già abilitato. Per impostazione predefinita, il provisioning automatico è abilitato per Windows 8 e Windows Server 2012.

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

 
