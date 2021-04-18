---
description: Apre un oggetto directory esistente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325672"
---
# <a name="ntopendirectoryobject-function"></a>NtOpenDirectoryObject (funzione)

\[Questa funzione può essere modificata o non disponibile in futuro.\]

Apre un oggetto directory esistente.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DirectoryHandle* \[ out\]
</dt> <dd>

Handle per l'oggetto directory appena aperto.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

[**\_ Maschera di accesso**](../secauthz/access-mask.md) che specifica l'accesso richiesto all'oggetto directory. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                      | Significato                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**Directory \_ di**</dt> <dt>0x0001</dt> query </dl>                                            | Eseguire query sull'accesso all'oggetto directory.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**Directory \_ di ATTRAVERSA**</dt> <dt>0x0002</dt> </dl>                                   | Accesso nome-ricerca all'oggetto directory.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**Directory \_ di Crea \_ oggetto**</dt> <dt>0x0004</dt> </dl>                   | Accesso per la creazione di nomi all'oggetto directory.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**Directory \_ di CREAZIONE della \_ sottodirectory**</dt> <dt>0x0008</dt> </dl> | Sottodirectory-creazione dell'accesso all'oggetto directory.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**Directory \_ di TUTTI \_**</dt> <dt>i diritti di accesso standard \_ \_ richiesti \| 0xF</dt> </dl> | Tutti i diritti precedenti e i **diritti standard sono \_ \_ obbligatori**.<br/> |



 

</dd> <dt>

*ObjectAttributes* \[ in\]
</dt> <dd>

Attributi per l'oggetto directory. Per inizializzare la struttura degli **\_ attributi dell'oggetto** , usare la macro **InitializeObjectAttributes** . Per ulteriori informazioni, vedere la documentazione relativa a questi elementi nella documentazione relativa a WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce lo stato \_ di esito positivo o uno stato di errore. I codici di stato possibili includono i seguenti.



| Codice restituito                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STATO \_ risorse insufficienti \_**</dt> </dl>    | Non è stato possibile allocare un buffer temporaneo richiesto da questa funzione.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**STATO \_ parametro non valido \_**</dt> </dl>         | Il parametro ObjectAttributes specificato è un puntatore **null** , non un puntatore valido a una struttura degli **\_ attributi degli oggetti** oppure alcuni membri specificati nella struttura degli **\_ attributi dell'oggetto** non sono validi.<br/>                                                                          |
| <dl> <dt>**\_nome oggetto \_ stato \_ non valido**</dt> </dl>      | Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** non valida perché è stata trovata una stringa vuota dopo il carattere **\_ \_ \_ separatore del percorso del nome dell'oggetto** .<br/>                                                                        |
| <dl> <dt>**\_nome oggetto \_ stato \_ non \_ trovato**</dt> </dl>   | Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** che non è stato trovato.<br/>                                                                                                                                                           |
| <dl> <dt>**il \_ percorso dell'oggetto stato non è stato \_ \_ \_ trovato**</dt> </dl>   | Il parametro *ObjectAttributes* contiene un membro **ObjectName** nella struttura degli **\_ attributi dell'oggetto** con un percorso dell'oggetto che non è stato trovato. <br/>                                                                                                                                      |
| <dl> <dt>**Stato \_ di sintassi del percorso dell'oggetto non \_ \_ \_ valida**</dt> </dl> | Il parametro *ObjectAttributes* non contiene un membro **RootDirectory** , ma il membro **ObjectName** nella struttura **degli \_ attributi dell'oggetto** è una stringa vuota o non contiene un **carattere \_ \_ \_ separatore del percorso del nome dell'oggetto** . Indica una sintassi non corretta per il percorso dell'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
