---
description: Reimposta il Archiviazione di autorizzazione SRK (Root Key) per essere compatibile con il sistema operativo.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Metodo ResetSrkAuth della Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 01f7536833529fd0d425f6064cfcdab11ac99c9cf1d6ab6ae7daf0c8b995d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004299"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a>Metodo ResetSrkAuth della classe \_ Win32 Tpm

Il **metodo ResetSrkAuth** della classe [**\_ Win32 Tpm**](win32-tpm.md) reimposta il valore di autorizzazione Archiviazione Root Key (SRK) in modo che sia compatibile con il sistema operativo.

## <a name="syntax"></a>Sintassi


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OwnerAuth* \[ in, facoltativo\]
</dt> <dd>

Tipo: **string**

Stringa che identifica il proprietario del TPM. Questa stringa deve essere una stringa con terminazione Null con codifica Base64 che contiene esattamente 20 byte di dati binari. Usare il [**metodo ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) per convertire una passphrase in questo formato previsto. Il *parametro OwnerAuth* viene letto dal Registro di sistema se non ne viene specificato nessuno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                         | Descrizione                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                                |
| <dl> <dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>             | Il valore di autorizzazione del proprietario specificato non può soddisfare la richiesta.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ DEFEND \_ LOCK \_ RUNNING**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | Il TPM è in difesa dagli attacchi con dizionario ed è in un periodo di timeout. Per altre informazioni, vedere il [**metodo ResetAuthLockOut.**](resetauthlockout-win32-tpm.md)<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
