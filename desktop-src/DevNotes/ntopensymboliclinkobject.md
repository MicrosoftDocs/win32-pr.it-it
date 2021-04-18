---
description: Apre un collegamento simbolico esistente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject (funzione)
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
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329049"
---
# <a name="ntopensymboliclinkobject-function"></a>NtOpenSymbolicLinkObject (funzione)

\[Questa funzione può essere modificata o non disponibile in futuro.\]

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

*LinkHandle* \[ out\]
</dt> <dd>

Handle per l'oggetto collegamento simbolico appena aperto.

</dd> <dt>

*DesiredAccess* \[ in\]
</dt> <dd>

[**\_ Maschera di accesso**](../secauthz/access-mask.md) che specifica l'accesso richiesto all'oggetto directory. È tipico utilizzare \_ la lettura generica in modo che sia possibile passare l'handle alla funzione [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .

</dd> <dt>

*ObjectAttributes* \[ in\]
</dt> <dd>

Attributi per l'oggetto directory. Per inizializzare la struttura degli **\_ attributi dell'oggetto** , usare la macro **InitializeObjectAttributes** . Se il chiamante non è in esecuzione in un contesto del thread di sistema, è necessario specificare il flag di **\_ \_ handle del kernel obj** durante l'inizializzazione della struttura. Per ulteriori informazioni, vedere la documentazione relativa a questi elementi nella documentazione relativa a WDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.

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

 

 
