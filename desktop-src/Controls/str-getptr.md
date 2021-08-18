---
title: Str_GetPtr funzione
description: Copia una stringa da un buffer a un altro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr controlli Windows funzione
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77c76ad276f6cb6dfc12bc272fbbc86c83617a0d00d36d77cf2ab0ca113811d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919451"
---
# <a name="str_getptr-function"></a>Funzione \_ GetPtr Str

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Copia una stringa da un buffer a un altro.

## <a name="syntax"></a>Sintassi


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszSource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a una stringa di origine.

</dd> <dt>

*pszDest* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore al buffer di destinazione. Questo valore può essere **NULL.**

</dd> <dt>

*cchDest* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Dimensione di *pszDest,* in caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se *pszDest* è NULL o *cchDest* è zero, restituisce le dimensioni del buffer, in caratteri, necessarie per contenere una copia con terminazione **Null** della stringa a cui punta *pszSource*.

Se *pszDest* è diverso da **NULL,** restituisce il numero di caratteri copiati correttamente, incluso il carattere Null di terminazione.

Se *pszDest* non può contenere l'intera stringa a cui punta *pszSource*, vengono copiati i caratteri (*cchDest*-1), viene restituita la stringa con terminazione Null e *cchDest.*

## <a name="remarks"></a>Commenti

**Str \_ GetPtr** è disponibile come versioni ANSI (**Str \_ GetPtrA**) e Unicode (**Str \_ GetPtrW**). Queste funzioni non vengono esportate per nome o dichiarate in un file di intestazione pubblico. Per usarli, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) da ComCtl32.dll per ottenere un puntatore a funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **Str \_ GetPtrW** (Unicode) e **Str \_ GetPtrA** (ANSI)<br/>                       |



 

