---
description: Il metodo IsOwnershipAllowed della classe Win32 Tpm indica se è consentita la possibilità di installare un proprietario \_ per il dispositivo.
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
ms.openlocfilehash: 81363f03280d7805ce965106c7af9f1b288ae75fd9217c4af85dd80f34973a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739551"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Metodo IsOwnershipAllowed della classe Tpm Win32 \_

Il **metodo IsOwnershipAllowed** della [**classe Win32 \_ Tpm**](win32-tpm.md) indica se è consentita la possibilità di installare un proprietario per il dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsOwnershipAllowed* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Se **true,** è consentita la possibilità di installare un proprietario per il dispositivo. Se **false,** il metodo [**TakeOwnership**](takeownership-win32-tpm.md) non installerà un proprietario per il dispositivo.

Questo valore può essere modificato con il [**metodo SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md) Il valore viene reimpostato **su true** dopo [**l'esecuzione del**](clear-win32-tpm.md) metodo Clear.

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
</dt> </dl>

 

 
