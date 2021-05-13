---
description: Enumera il contenuto dell'elenco degli elementi usati più di recente. Recupera facoltativamente un elemento dall'enumerazione .
title: Funzione EnumMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 1e6e4bd0820d35fec2a108a81eb1030567493e6a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843162"
---
# <a name="enummrulistw-function"></a>Funzione EnumMRUListW

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. \]

Enumera il contenuto dell'elenco degli elementi usati più di recente. Recupera facoltativamente un elemento dall'enumerazione .

## <a name="syntax"></a>Sintassi


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMRU* \[ Pollici\]
</dt> <dd>

Tipo: **HANDLE**

Handle dell'elenco MRU, ottenuto al momento della creazione dell'elenco.

</dd> <dt>

*nItem* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Elemento da restituire. Se questo valore è minore di 0, la funzione restituisce il numero di elementi nell'elenco MRU.

</dd> <dt>

*lpData* \[ Cambio\]
</dt> <dd>

Tipo: **\* void**

Puntatore a un buffer che riceve l'elemento richiesto in *nItem.* Se *nItem* è minore di 0, il contenuto di questo buffer rimane invariato.

</dd> <dt>

*uLen* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensione del buffer, incluso il carattere Null di terminazione. Se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** questa è la dimensione in byte. In caso contrario, è la dimensione in caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce uno dei valori seguenti.

-   Restituisce il numero di elementi nell'enumerazione, se *nItem* è minore di 0.
-   Restituisce -1 se si è verificato un errore.
-   In caso contrario, restituisce le dimensioni della stringa restituita in *lpData*, incluso il carattere Null di terminazione. Se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** questa è la dimensione in byte. In caso contrario, è la dimensione in caratteri.

## <a name="remarks"></a>Commenti

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 403 per **EnumMRUListW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
