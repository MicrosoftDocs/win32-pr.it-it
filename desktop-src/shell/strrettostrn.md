---
description: Accetta una struttura STRRET restituita da IShellFolder::GetDisplayNameOf, la converte in una stringa e inserisce il risultato in un buffer.
title: Funzione StrRetToStrN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841032"
---
# <a name="strrettostrn-function"></a>Funzione StrRetToStrN

Accetta una [**struttura STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) restituita da [**IShellFolder::GetDisplayNameOf,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)la converte in una stringa e inserisce il risultato in un buffer.

## <a name="syntax"></a>Sintassi


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszOut* \[ Cambio\]
</dt> <dd>

Tipo: **LPTSTR**

Buffer in cui contenere il nome visualizzato. Verrà restituito come stringa con terminazione Null. Se *cchOut* è troppo piccolo, il nome verrà troncato per adattarsi.

</dd> <dt>

*cchOut* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensione di *pszOut,* in caratteri. Se *cchOut* è troppo piccolo, la stringa verrà troncata per adattarsi.

</dd> <dt>

*pStrRet* \[ in, out\]
</dt> <dd>

Tipo: **LPSTRRET**

Puntatore a una [**struttura STRRET.**](/windows/desktop/api/Shtypes/ns-shtypes-strret) Quando la funzione viene restituita, questo puntatore non sarà più valido.

</dd> <dt>

*pidl* \[ Pollici\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore alla struttura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

**TRUE per** l'esito positivo, **FALSE** per l'errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> A Shell32.dll versione 5.0, chiamare questa funzione equivale a chiamare [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**StrRetToStrN** non viene esportato in base al nome. Per usarlo, è necessario usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 96 Shell32.dll per ottenere un puntatore a funzione.

Se il **membro uType** della struttura a cui punta *pStrRet* è impostato su **STRRET \_ WSTR,** il membro **pOleStr** di tale struttura verrà liberato in caso di restituzione.

Si noti che questa funzione viene esportata da Shell32.dll anziché da Shlwapi.dll. È incluso anche in Shlobj.h anziché in Shlwapi.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 2000 Professional e Windows XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
