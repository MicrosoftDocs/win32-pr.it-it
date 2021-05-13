---
description: Aggiunge una stringa all'inizio dell'elenco MRU (Most Recently Used).
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
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841192"
---
# <a name="addmrustringw-function"></a>Funzione AddMRUStringW

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere stato modificato o non disponibile nelle versioni successive di Windows. \]

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

Puntatore ai dati. Può trattarsi di una stringa o, se l'elenco MRU è stato creato con il flag **\_ BINARY MRU,** dati binari. Nel caso di dati binari, il primo **valore DWORD** ne indica le dimensioni.

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



 

