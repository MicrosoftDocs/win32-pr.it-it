---
description: Crea la chiave del Registro di sistema specificata in un hive del Registro di sistema offline. Se la chiave esiste già, la funzione la apre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Funzione ORCreateKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7ea5a365a9c5bdcb478ce47443a713ed5bc091666b54de880dc478708e4c36c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749691"
---
# <a name="orcreatekey-function"></a>ORCreateKey - funzione

Crea la chiave del Registro di sistema specificata in un hive del Registro di sistema offline. Se la chiave esiste già, la funzione la apre.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle per una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*lpSubKey* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nome di una sottochiave che questa funzione apre o crea. Il *parametro lpSubKey* deve specificare una sottochiave della chiave identificata dal *parametro Handle.* può avere una profondità fino a 32 livelli nell'albero del Registro di sistema. Per altre informazioni sui nomi delle chiavi, vedere [Struttura del Registro di sistema.](../sysinfo/structure-of-the-registry.md)

Questo parametro non può essere **NULL.**

I nomi delle chiavi non supportano la distinzione tra maiuscole e minuscole.

</dd> <dt>

*lpClass* \[ in, facoltativo\]
</dt> <dd>

Classe (tipo di oggetto) di questa chiave. Questo parametro può essere ignorato. Questo parametro può essere **NULL**.

</dd> <dt>

*dwOptions* \[ in, facoltativo\]
</dt> <dd>

Questo parametro può essere 0 o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**REG \_ OPTION \_ CREATE \_ LINK**</dt> <dt>0x000000002L</dt> </dl>    | La chiave è un collegamento simbolico. Il percorso di destinazione viene assegnato al valore L"SymbolicLinkValue" della chiave. Il percorso di destinazione deve essere un percorso assoluto del Registro di sistema. Se questa opzione è impostata, **è necessario impostare anche REG OPTION NON \_ \_ \_ VOLATILE.** <br/> Se il *parametro lpSubKey* specifica una chiave esistente, deve essere stata creata con **REG OPTION CREATE \_ \_ \_ LINK.**<br/> I collegamenti simbolici del Registro di sistema devono essere usati solo quando sono assolutamente necessari per la compatibilità delle applicazioni. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**REG \_ OPTION \_ NON \_ VOLATILE**</dt> <dt>0x00000000L</dt> </dl> | La chiave non è volatile. si tratta dell'impostazione predefinita. Le informazioni vengono archiviate in un file e mantenute al riavvio del sistema. La [**funzione ORSaveHive**](orsavehive.md) salva le chiavi non volatili.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [struttura SECURITY \_ DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) che contiene un descrittore di sicurezza per la nuova chiave. Se *pSecurityDescriptor* è **NULL,** la chiave ottiene un descrittore di sicurezza predefinito. Gli ACL in un descrittore di sicurezza predefinito per una chiave vengono ereditati dalla relativa chiave padre diretta.

</dd> <dt>

*phkResult* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave aperta o creata. Usare la [**funzione ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.

</dd> <dt>

*pdwDisposition* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve uno dei valori di disposizione seguenti.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**REG \_ CREATED \_ NEW \_ KEY**</dt> <dt>0x00000001L</dt> </dl>             | La chiave non esiste ed è stata creata.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**REG \_ OPENED \_ EXISTING \_ KEY**</dt> <dt>0x000000002L</dt> </dl> | La chiave esisteva ed era semplicemente aperta senza essere modificata.<br/> |



 

Se *pdwDisposition è* **NULL,** non vengono restituite informazioni sulla disposizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

Se il *parametro dwOptions* è impostato con **REG OPTION CREATE \_ \_ \_ LINK** ma **REG OPTION NON \_ \_ \_ VOLATILE** è deselezionato o se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce ERROR \_ INVALID \_ PARAMETER.

## <a name="remarks"></a>Commenti

La chiave creata **dalla funzione ORCreateKey** non ha valori. Un'applicazione può usare la [**funzione ORSetValue**](orsetvalue.md) per impostare i valori delle chiavi.

La **funzione ORCreateKey** non può essere usata per creare la chiave radice in un hive del Registro di sistema offline. Usare la [**funzione ORCreateHive**](orcreatehive.md) per creare la chiave radice e ottenere un handle per la chiave.

Il Registro di sistema offline non supporta il salvataggio di singole chiavi. Usare la [**funzione ORSaveHive**](orsavehive.md) per salvare una chiave e le relative sottochiavi in un hive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[DESCRITTORE \_ DI SICUREZZA](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
