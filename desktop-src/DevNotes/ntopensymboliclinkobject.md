---
description: Apre un collegamento simbolico esistente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Funzione NtOpenSymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 1713d12763eaaa5c43b4ef27f3d8843eefd3ba86f0a8ddfea9dfaecd9d01b10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003762"
---
# <a name="ntopensymboliclinkobject-function"></a>Funzione NtOpenSymbolicLinkObject

\[Questa funzione potrebbe essere modificata o non disponibile in futuro.\]

Apre un collegamento simbolico esistente.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LinkHandle* \[ Cambio\]
</dt> <dd>

Handle per l'oggetto collegamento simbolico appena aperto.

</dd> <dt>

*DesiredAccess* \[ Pollici\]
</dt> <dd>

MASCHERA [**DI \_ ACCESSO che**](../secauthz/access-mask.md) specifica l'accesso richiesto all'oggetto directory. In genere si usa GENERIC \_ READ in modo che l'handle possa essere passato alla funzione [**NtQueryDirectoryObject.**](ntquerydirectoryobject.md)

</dd> <dt>

*ObjectAttributes* \[ Pollici\]
</dt> <dd>

Attributi per l'oggetto directory. Per inizializzare la **struttura OBJECT \_ ATTRIBUTES,** usare la macro **InitializeObjectAttributes.** Se il chiamante non è in esecuzione in un contesto del thread di sistema, deve specificare il flag **OBJ \_ KERNEL \_ HANDLE** durante l'inizializzazione della struttura. Per altre informazioni, vedere la documentazione relativa a questi elementi nella documentazione per WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **STATUS \_ SUCCESS o** uno stato di errore.

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

 

 
