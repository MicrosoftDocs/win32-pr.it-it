---
description: Crea la chiave del registro di sistema specificata in un hive del registro di sistema offline. Se la chiave esiste già, la funzione la apre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Funzione ORCreateKey (offreg. h)
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
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331957"
---
# <a name="orcreatekey-function"></a>ORCreateKey (funzione)

Crea la chiave del registro di sistema specificata in un hive del registro di sistema offline. Se la chiave esiste già, la funzione la apre.

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

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpSubKey* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nome di una sottochiave che la funzione apre o crea. Il parametro *lpSubKey* deve specificare una sottochiave della chiave identificata dal parametro *handle* . può essere fino a 32 livelli di profondità nell'albero del registro di sistema. Per ulteriori informazioni sui nomi delle chiavi, vedere [la struttura del registro di sistema](../sysinfo/structure-of-the-registry.md).

Questo parametro non può essere **null**.

Per i nomi di chiave non viene fatta distinzione tra maiuscole

</dd> <dt>

*lpClass* \[ in, facoltativo\]
</dt> <dd>

Classe (tipo di oggetto) della chiave. Questo parametro può essere ignorato. Questo parametro può essere **NULL**.

</dd> <dt>

*dwOptions* \[ in, facoltativo\]
</dt> <dd>

Questo parametro può essere 0 o uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**Reg \_ OPZIONE \_ Crea \_ collegamento**</dt> <dt>0x00000002L</dt> </dl>    | La chiave è un collegamento simbolico. Il percorso di destinazione viene assegnato al valore L "SymbolicLinkValue" della chiave. Il percorso di destinazione deve essere un percorso assoluto del registro di sistema. Se questa opzione è impostata, è necessario impostare anche l' **\_ opzione reg \_ non \_ volatile** . <br/> Se il parametro *lpSubKey* specifica una chiave esistente, deve essere stato creato con il **\_ \_ \_ collegamento reg Option create**.<br/> I collegamenti simbolici del registro di sistema devono essere usati solo quando sono assolutamente necessari per la compatibilità delle applicazioni. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**Reg \_ OPZIONE \_ non \_ volatile**</dt> <dt>0x00000000L</dt> </dl> | La chiave non è volatile; si tratta dell'impostazione predefinita. Le informazioni vengono archiviate in un file e mantenute al riavvio del sistema. La funzione [**ORSaveHive**](orsavehive.md) Salva le chiavi che non sono volatili.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura [di \_ descrittori di sicurezza](/windows/win32/api/winnt/ns-winnt-security_descriptor) che contiene un descrittore di sicurezza per la nuova chiave. Se *pSecurityDescriptor* è **null**, la chiave ottiene un descrittore di sicurezza predefinito. Gli ACL in un descrittore di sicurezza predefinito per una chiave vengono ereditati dalla relativa chiave padre diretta.

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave aperta o creata. Usare la funzione [**ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.

</dd> <dt>

*pdwDisposition* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile che riceve uno dei seguenti valori di disposizione.



| Valore                                                                                                                                                                                                                                                          | Significato                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**Reg \_ CREAZIONE della \_ nuova \_ chiave**</dt> <dt>0x00000001L</dt> </dl>             | La chiave non esiste ed è stata creata.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**Reg \_ 0x00000002L \_ \_ chiave esistente aperta**</dt> <dt></dt> </dl> | La chiave esisteva ed è stata semplicemente aperta senza essere modificata.<br/> |



 

Se *pdwDisposition* è **null**, non viene restituita alcuna informazione sulla disposizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se il parametro *dwOptions* è impostato con **l' \_ opzione reg \_ Create \_ link** ma l' **opzione reg \_ \_ non \_ volatile** è deselezionata, oppure se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce l'errore \_ parametro non valido \_ .

## <a name="remarks"></a>Commenti

La chiave creata dalla funzione **ORCreateKey** non contiene valori. Per impostare i valori delle chiavi, un'applicazione può usare la funzione [**ORSetValue**](orsetvalue.md) .

Non è possibile usare la funzione **ORCreateKey** per creare la chiave radice in un hive del registro di sistema offline. Usare la funzione [**ORCreateHive**](orcreatehive.md) per creare la chiave radice e ottenere un handle per la chiave.

Il registro offline non supporta il salvataggio di singole chiavi. Usare la funzione [**ORSaveHive**](orsavehive.md) per salvare una chiave e le relative sottochiavi in hive.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

[descrittore di sicurezza \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
