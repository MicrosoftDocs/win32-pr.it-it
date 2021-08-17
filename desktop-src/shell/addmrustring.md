---
description: Aggiunge una stringa all'inizio dell'elenco degli elementi usati più di recente.
title: Funzione AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 4ac72c44b670466f10cd708b81b1a84f93a349afcb0d81473ed5e6578c20617a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861593"
---
# <a name="addmrustringw-function"></a>Funzione AddMRUStringW

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. \]

Aggiunge una stringa all'inizio dell'elenco degli elementi usati più di recente.

## <a name="syntax"></a>Sintassi


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMRU* \[ Pollici\]
</dt> <dd>

Tipo: **HANDLE**

Handle dell'elenco MRU.

</dd> <dt>

*szString* \[ Pollici\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore ai dati. Può trattarsi di una stringa o, se l'elenco MRU è stato creato con il flag **BINARY MRU, \_** dati binari. Nel caso di dati binari, il primo **valore DWORD** ne indica le dimensioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce un valore non negativo in caso di esito positivo, -1 in caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. È possibile accedervi tramite [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 401 per **AddMRUStringW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

