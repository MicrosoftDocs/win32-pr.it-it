---
title: Funzione Str_GetPtr
description: Copia una stringa da un buffer a un altro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Controlli di Windows per la funzione Str_GetPtr
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
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740511"
---
# <a name="str_getptr-function"></a>Str \_ Getptr (funzione)

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

*pszSource* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore a una stringa di origine.

</dd> <dt>

*pszDest* \[ in uscita\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Puntatore al buffer di destinazione. Questo valore può essere **null**.

</dd> <dt>

*cchDest* \[ in\]
</dt> <dd>

Tipo: **int**

Dimensioni di *pszDest*, in caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Se *pszDest* è **null** o *cchDest* è zero, restituisce la dimensione del buffer, in caratteri, necessaria per contenere una copia con terminazione null della stringa a cui punta *pszSource*.

Se *pszDest* è diverso da **null**, restituisce il numero di caratteri copiati correttamente, incluso il carattere null di terminazione.

Se *pszDest* non è in grado di mantenere l'intera stringa a cui punta *pszSource*, vengono copiati i caratteri (*cchDest*-1), la stringa con terminazione null e *cchDest* restituito.

## <a name="remarks"></a>Commenti

**Str \_ GetPtr** è disponibile come versione ANSI (**Str \_ GetPtrA**) e Unicode (**Str \_ GetPtrW**). Queste funzioni non vengono esportate in base al nome o dichiarate in un file di intestazione pubblico. Per usarli, è necessario usare [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere il numero ordinale 233 (**Str \_ GetPtrA**) o 235 (**Str \_ GetPtrW**) da ComCtl32.dll per ottenere un puntatore a funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **Str \_ GetPtrW** (Unicode) e **Str \_ GetPtrA** (ANSI)<br/>                       |



 

