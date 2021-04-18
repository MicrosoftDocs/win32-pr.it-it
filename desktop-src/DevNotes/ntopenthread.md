---
description: Apre un handle per un oggetto thread con l'accesso specificato.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread (funzione)
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
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328276"
---
# <a name="ntopenthread-function"></a>NtOpenThread (funzione)

\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso. Usare invece la funzione [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]

Apre un handle per un oggetto thread con l'accesso specificato.

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

*ThreadHandle* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve l'handle dell'oggetto thread.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

Tipo di dati di una [**\_ maschera di accesso**](../secauthz/access-mask-format.md) che fornisce i tipi di accesso desiderati per l'oggetto thread.

</dd> <dt>

*ObjectAttributes* \[ in\]
</dt> <dd>

Puntatore a una struttura [degli \_ attributi dell'oggetto](https://msdn.microsoft.com/library/aa491657.aspx) . Il membro **ObjectName** di questa struttura deve essere null.

**Windows Server 2003 e Windows XP:** Il membro **ObjectName** di questa struttura può puntare a un nome di oggetto. Se **ObjectName** non è null, il parametro *ClientID* deve essere null.

</dd> <dt>

*ClientID* \[ in\]
</dt> <dd>

Puntatore a una struttura **di \_ ID client** che identifica il thread di cui deve essere aperto il thread.

**Windows Server 2003 e Windows XP:** Puntatore a una struttura **di \_ ID client** che identifica il thread di cui deve essere aperto il thread. Questo parametro può essere NULL. Se questo parametro non è NULL, il membro **ObjectName** della struttura a cui punta il parametro *OBJECTATTRIBUTES* deve essere null.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice **NTSTATUS** o Error.

I moduli e il significato dei codici di errore **NTSTATUS** sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll. lib è disponibile in WDK. È anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per eseguire un collegamento dinamico a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
