---
description: Esegue un test automatico del TPM e restituisce il risultato.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Metodo SelfTest della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306375"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a>Metodo SelfTest della \_ classe TPM Win32

Il metodo **SELFTEST** della classe [**\_ TPM Win32**](win32-tpm.md) esegue un test automatico del TPM e restituisce il risultato.

Un self-test TPM viene eseguito automaticamente all'avvio del computer.

## <a name="syntax"></a>Sintassi


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SelfTestResult* \[ out\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di byte che contiene il risultato di test automatico. Il formato di questo parametro è specifico del produttore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                 | Descrizione                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
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

 

 
