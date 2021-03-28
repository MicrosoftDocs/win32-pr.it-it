---
description: Aggiunge una stringa all'inizio dell'elenco degli ultimi elementi usati (MRU).
title: AddMRUStringW (funzione)
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049374"
---
# <a name="addmrustringw-function"></a>AddMRUStringW (funzione)

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. \]

Aggiunge una stringa all'inizio dell'elenco degli ultimi elementi usati (MRU).

## <a name="syntax"></a>Sintassi


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMRU* \[ in\]
</dt> <dd>

Tipo: **handle**

Handle dell'elenco MRU.

</dd> <dt>

*szString* \[ in\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntatore ai dati. Può essere una stringa o, se l'elenco MRU è stato creato con il flag **\_ binario MRU** , dati binari. Nel caso dei dati binari, il primo **valore DWORD** ne indica le dimensioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce un valore non negativo se ha esito positivo,-1 in caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. È possibile accedervi tramite [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o estratti da comctl32.dll in base al relativo ordinale, ovvero 401 per **AddMRUStringW**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5,0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

