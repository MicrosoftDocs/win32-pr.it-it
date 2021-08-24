---
description: Indica l'azione utente necessaria per eseguire l'Trusted Platform Module di presenza fisica (TPM). Usare il metodo SetPhysicalPresenceRequest per richiedere un'operazione.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Metodo GetPhysicalPresenceTransition della Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 939f29d923182d3e2b0b9237c49c2a5fc6ff8652d2361f867a7e95af48415654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906341"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Metodo GetPhysicalPresenceTransition della classe Tpm Win32 \_

Il **metodo GetPhysicalPresenceTransition** della classe [**\_ Tpm Win32**](win32-tpm.md) indica l'azione utente necessaria per eseguire l'operazione di presenza fisica Trusted Platform Module (TPM). Usare il [**metodo SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione. L'azione utente richiesta viene impostata per il computer al momento della produzione. In genere è necessario un riavvio del computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Transizione* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Valore intero che specifica la transizione necessaria per eseguire un'operazione di presenza fisica TPM.



| Valore                                                                        | Significato                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non è necessaria alcuna azione dell'utente per eseguire un'operazione di presenza fisica TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Per eseguire un'operazione di presenza fisica TPM, l'utente deve arrestare il computer e quindi riattivarlo usando il pulsante di alimentazione. L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Per eseguire un'operazione di presenza fisica TPM, l'utente deve riavviare il computer usando un riavvio a caldo. L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | L'azione utente richiesta è sconosciuta.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Il metodo è stato eseguito correttamente.<br/>                                                            |
| <dl> <dt>**TPM \_ Errore \_ E PPI \_ ACPI \_**</dt> 2150171392 <dt>(0x80290300)</dt> </dl> | Si è verificato un errore hardware. Per altre informazioni, vedere il produttore del computer.<br/> |



 

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

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
