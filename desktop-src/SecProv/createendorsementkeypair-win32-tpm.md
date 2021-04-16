---
description: Crea una coppia di chiavi di approvazione a 2048 bit nel TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Metodo CreateEndorsementKeyPair della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525692"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Metodo CreateEndorsementKeyPair della \_ classe TPM Win32

Il metodo **CreateEndorsementKeyPair** della classe [**\_ TPM Win32**](win32-tpm.md) crea una coppia di chiavi di approvazione a 2048 bit nel TPM. Per eseguire correttamente il metodo [**TakeOwnership**](takeownership-win32-tpm.md) , è necessario che la coppia di chiavi di verifica dell'autenticità sia disponibile. È possibile utilizzare il metodo [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) per rilevare se la chiave di verifica dell'autenticità esiste già nel TPM.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                          |
| <dl> <dt> **TPM \_ E \_ disabilitato \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Una coppia di chiavi di verifica dell'autenticità esiste già nel TPM.<br/> |



 

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

 

 
