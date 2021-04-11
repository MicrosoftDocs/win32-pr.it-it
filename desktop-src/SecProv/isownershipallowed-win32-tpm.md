---
description: Il metodo IsOwnershipAllowed della \_ classe TPM Win32 indica se è consentita la possibilità di installare un proprietario per il dispositivo.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Metodo IsOwnershipAllowed della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226005"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Metodo IsOwnershipAllowed della \_ classe TPM Win32

Il metodo **IsOwnershipAllowed** della classe [**\_ TPM Win32**](win32-tpm.md) indica se è consentita la possibilità di installare un proprietario per il dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsOwnershipAllowed* \[ out\]
</dt> <dd>

Tipo: **booleano**

Se **true**, è consentita la possibilità di installare un proprietario per il dispositivo. Se **false**, il metodo [**TakeOwnership**](takeownership-win32-tpm.md) non riuscirà a installare un proprietario per il dispositivo.

Questo valore può essere modificato con il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) . Il valore viene reimpostato su **true** dopo l'esecuzione del metodo [**Clear**](clear-win32-tpm.md) .

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
</dt> </dl>

 

 
