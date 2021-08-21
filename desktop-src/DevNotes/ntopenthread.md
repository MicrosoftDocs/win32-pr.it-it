---
description: Apre un handle a un oggetto thread con l'accesso specificato.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Funzione NtOpenThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e5f459b12d90a12b7c75aabd44d25f6fcf352aff8914e6d991471acaee400260
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079691"
---
# <a name="ntopenthread-function"></a>Funzione NtOpenThread

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriori comunicazioni. In [**alternativa, usare la funzione OpenThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)\]

Apre un handle a un oggetto thread con l'accesso specificato.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ThreadHandle* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve l'handle dell'oggetto thread.

</dd> <dt>

*DesiredAccess* \[ Pollici\]
</dt> <dd>

Tipo [**di dati ACCESS \_ MASK**](../secauthz/access-mask-format.md) che fornisce i tipi di accesso desiderati per l'oggetto thread.

</dd> <dt>

*ObjectAttributes* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura OBJECT \_ ATTRIBUTES.](https://msdn.microsoft.com/library/aa491657.aspx) Il **membro ObjectName** di questa struttura deve essere NULL.

**Windows Server 2003 e Windows XP:** Il **membro ObjectName** di questa struttura può puntare a un nome di oggetto. Se **ObjectName** non è NULL, il *parametro ClientId* deve essere NULL.

</dd> <dt>

*ClientId* \[ Pollici\]
</dt> <dd>

Puntatore a una **struttura \_ CLIENT ID** che identifica il thread di cui deve essere aperto il thread.

**Windows Server 2003 e Windows XP:** Puntatore a una **struttura \_ CLIENT ID** che identifica il thread di cui deve essere aperto il thread. Questo parametro può essere NULL. Se questo parametro non è NULL, il **membro ObjectName** della struttura a cui punta il *parametro ObjectAttributes* deve essere NULL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **NTSTATUS o** un codice di errore.

I formati e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus.h disponibile nel WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile nel WDK. È anche possibile usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
