---
description: Indica l'azione dell'utente necessaria per eseguire l'operazione di presenza fisica Trusted Platform Module (TPM). Usare il metodo SetPhysicalPresenceRequest per richiedere un'operazione.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Metodo GetPhysicalPresenceTransition della classe Win32_Tpm
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
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316102"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Metodo GetPhysicalPresenceTransition della \_ classe TPM Win32

Il metodo **GetPhysicalPresenceTransition** della classe [**\_ TPM Win32**](win32-tpm.md) indica l'azione dell'utente necessaria per eseguire l'operazione di presenza fisica Trusted Platform Module (TPM). Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione. L'azione richiesta dell'utente è impostata per il computer al momento della fabbricazione. In genere è necessario riavviare il computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Transizione* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Valore integer che specifica la transizione necessaria per eseguire un'operazione di presenza fisica del TPM.



| Valore                                                                        | Significato                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non è necessaria alcuna azione dell'utente per eseguire un'operazione di presenza fisica TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Per eseguire un'operazione di presenza fisica TPM, l'utente deve arrestare il computer e quindi riattivarlo utilizzando il pulsante di alimentazione. L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Per eseguire un'operazione di presenza fisica TPM, l'utente deve riavviare il computer utilizzando un riavvio a caldo. L'utente deve essere fisicamente presente nel computer per accettare o rifiutare la modifica quando richiesto dal BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | L'azione obbligatoria dell'utente è sconosciuta.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Il metodo è stato eseguito correttamente.<br/>                                                            |
| <dl> <dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Si è verificato un errore hardware. Per ulteriori informazioni, consultare il produttore del computer.<br/> |



 

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

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
