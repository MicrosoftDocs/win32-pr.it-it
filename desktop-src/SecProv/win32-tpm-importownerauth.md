---
description: Importa le informazioni di autorizzazione del proprietario per un TPM già di proprietà nel registro di sistema del sistema operativo.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Metodo Win32_Tpm:: ImportOwnerAuth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966580"
---
# <a name="win32_tpmimportownerauth-method"></a>\_Metodo Win32 TPM:: ImportOwnerAuth

Importa le informazioni di autorizzazione del proprietario per un TPM già di proprietà nel registro di sistema del sistema operativo. Questa operazione convaliderà prima di tutto se le informazioni di autorizzazione del proprietario fornite sono corrette. Se è corretto, il metodo importa queste informazioni nel registro di sistema.

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerAuth* \[ in\]
</dt> <dd>

Informazioni di autorizzazione del proprietario valide per il TPM.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo è particolarmente utile negli scenari in cui il TPM è in uno stato "pronto con funzionalità ridotte" e richiede l'importazione dell'autorizzazione del proprietario in modo che sia completamente pronto o in scenari a doppio avvio in cui uno dei sistemi operativi è proprietario del TPM e le informazioni di autorizzazione del proprietario per TPM non sono disponibili nell'altro sistema operativo.

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

 

 
