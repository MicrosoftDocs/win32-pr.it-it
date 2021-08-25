---
description: Apre un oggetto directory esistente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Funzione NtOpenDirectoryObject
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
ms.openlocfilehash: ddfe43bab114af968de76673f08f2e301f775e2e7475e7b17a2e08004ef50dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003792"
---
# <a name="ntopendirectoryobject-function"></a>Funzione NtOpenDirectoryObject

\[Questa funzione potrebbe essere modificata o non disponibile in futuro.\]

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

*DirectoryHandle* \[ Cambio\]
</dt> <dd>

Handle per l'oggetto directory appena aperto.

</dd> <dt>

*DesiredAccess* \[ Pollici\]
</dt> <dd>

MASCHERA [**DI \_ ACCESSO che**](../secauthz/access-mask.md) specifica l'accesso richiesto all'oggetto directory. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                      | Significato                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**DIRECTORY \_ Query**</dt> <dt>0x0001</dt> </dl>                                            | Eseguire query sull'accesso all'oggetto directory.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**DIRECTORY \_ Attraversa**</dt> <dt>0x0002</dt> </dl>                                   | Accesso name-lookup all'oggetto directory.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**DIRECTORY \_ Create \_ OBJECT**</dt> <dt>0x0004</dt> </dl>                   | Accesso di creazione del nome all'oggetto directory.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**DIRECTORY \_ CREATE \_ SUBDIRECTORY**</dt> <dt>0x0008</dt> </dl> | Accesso alla creazione di sottodirectory all'oggetto directory.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**DIRECTORY \_ TUTTI \_ I DIRITTI**</dt> STANDARD DI ACCESSO RICHIESTI <dt> \_ \_ \| 0XF</dt> </dl> | Tutti i diritti precedenti più **STANDARD \_ RIGHTS \_ REQUIRED**.<br/> |



 

</dd> <dt>

*ObjectAttributes* \[ Pollici\]
</dt> <dd>

Attributi per l'oggetto directory. Per inizializzare la **struttura OBJECT \_ ATTRIBUTES,** usare la macro **InitializeObjectAttributes.** Per altre informazioni, vedere la documentazione relativa a questi elementi nella documentazione per WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce STATUS \_ SUCCESS o uno stato di errore. I codici di stato possibili includono i seguenti.



| Codice restituito                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**RISORSE \_ INSUFFICIENTI DI \_ STATO**</dt> </dl>    | Impossibile allocare un buffer temporaneo richiesto da questa funzione.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**STATO \_ PARAMETRO NON \_ VALIDO**</dt> </dl>         | Il parametro ObjectAttributes specificato era un **puntatore NULL,** non un puntatore valido a una struttura **OBJECT \_ ATTRIBUTES** oppure alcuni membri specificati nella struttura **OBJECT \_ ATTRIBUTES** non erano validi.<br/>                                                                          |
| <dl> <dt>**NOME \_ OGGETTO DI STATO NON \_ \_ VALIDO**</dt> </dl>      | Il *parametro ObjectAttributes* conteneva un membro **ObjectName** nella struttura **OBJECT \_ ATTRIBUTES** non valido perché è stata trovata una stringa vuota dopo il carattere **OBJECT NAME PATH \_ \_ \_ SEPARATOR.**<br/>                                                                        |
| <dl> <dt>**NOME \_ OGGETTO DI STATO NON \_ \_ \_ TROVATO**</dt> </dl>   | Il *parametro ObjectAttributes* conteneva un **membro ObjectName** nella struttura **OBJECT \_ ATTRIBUTES** che non è stato trovato.<br/>                                                                                                                                                           |
| <dl> <dt>**PERCORSO \_ \_ DELL'OGGETTO \_ DI STATO NON \_ TROVATO**</dt> </dl>   | Il *parametro ObjectAttributes* conteneva un **membro ObjectName** nella struttura **OBJECT \_ ATTRIBUTES** con un percorso oggetto che non è stato trovato. <br/>                                                                                                                                      |
| <dl> <dt>**STATO \_ SINTASSI \_ DEL PERCORSO OGGETTO NON \_ \_ VALIDA**</dt> </dl> | Il *parametro ObjectAttributes* non contiene un membro **RootDirectory,** ma il membro **ObjectName** nella struttura **OBJECT \_ ATTRIBUTES** è una stringa vuota o non contiene un carattere **OBJECT NAME PATH \_ \_ \_ SEPARATOR.** Indica una sintassi non corretta per il percorso dell'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
