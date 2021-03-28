---
description: Enumera il contenuto dell'elenco degli ultimi elementi usati (MRU). Consente, facoltativamente, di recuperare un elemento dall'enumerazione.
title: EnumMRUListW (funzione)
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
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884393"
---
# <a name="enummrulistw-function"></a>EnumMRUListW (funzione)

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. \]

Enumera il contenuto dell'elenco degli ultimi elementi usati (MRU). Consente, facoltativamente, di recuperare un elemento dall'enumerazione.

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

*hMRU* \[ in\]
</dt> <dd>

Tipo: **handle**

Handle dell'elenco MRU, ottenuto quando è stato creato l'elenco.

</dd> <dt>

*Niten* \[ in\]
</dt> <dd>

Tipo: **int**

Elemento da restituire. Se questo valore è minore di 0, la funzione restituisce il numero di elementi nell'elenco MRU.

</dd> <dt>

*lpData* \[ out\]
</dt> <dd>

Tipo: **void \** _

Puntatore a un buffer che riceve l'elemento richiesto in _nItem *. Se il numero di *Nite* è minore di 0, il contenuto di questo buffer è invariato.

</dd> <dt>

*uLen* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni del buffer, incluso il carattere null di terminazione. Se l'elenco MRU è stato creato con il flag **\_ binario MRU** , corrisponde alle dimensioni in byte. In caso contrario, è la dimensione in caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce uno dei valori seguenti.

-   Restituisce il numero di elementi nell'enumerazione, se *nitet* è minore di 0.
-   Restituisce-1 se si è verificato un errore.
-   In caso contrario, restituisce le dimensioni della stringa restituita in *lpData*, incluso il carattere null di terminazione. Se l'elenco MRU è stato creato con il flag **\_ binario MRU** , corrisponde alle dimensioni in byte. In caso contrario, è la dimensione in caratteri.

## <a name="remarks"></a>Commenti

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estratti da comctl32.dll in base al relativo ordinale, ovvero 403 per **EnumMRUListW**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
