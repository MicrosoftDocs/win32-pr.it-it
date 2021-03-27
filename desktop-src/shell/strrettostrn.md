---
description: 'Accetta una struttura STRRET restituita da IShellFolder:: GetDisplayNameOf, la converte in una stringa e inserisce il risultato in un buffer.'
title: StrRetToStrN (funzione)
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
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995173"
---
# <a name="strrettostrn-function"></a>StrRetToStrN (funzione)

Accetta una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) restituita da [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), la converte in una stringa e inserisce il risultato in un buffer.

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

*pszOut* \[ out\]
</dt> <dd>

Tipo: **LPTSTR**

Buffer in cui memorizzare il nome visualizzato. Verrà restituito come stringa con terminazione null. Se *cchOut* è troppo piccolo, il nome verrà troncato per adattarlo.

</dd> <dt>

*cchOut* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni di *pszOut*, in caratteri. Se *cchOut* è troppo piccolo, la stringa verrà troncata per essere adattata.

</dd> <dt>

*pStrRet* \[ in uscita\]
</dt> <dd>

Tipo: **LPSTRRET**

Puntatore a una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Quando la funzione restituisce, il puntatore non sarà più valido.

</dd> <dt>

*PIDL* \[ in\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore alla struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

**True** per l'esito positivo, **false** per l'errore.

## <a name="remarks"></a>Commenti

> [!Note]  
> A partire da Shell32.dll versione 5,0, la chiamata a questa funzione equivale alla chiamata a [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**StrRetToStrN** non viene esportato in base al nome. Per usarlo, è necessario usare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e richiedere l'ordinale 96 da Shell32.dll per ottenere un puntatore a funzione.

Se il membro **uType** della struttura a cui punta *pStrRet* è impostato su **STRRET \_ WSTR**, il membro **pOleStr** di tale struttura verrà liberato al ritorno.

Si noti che questa funzione viene esportata da Shell32.dll anziché da Shlwapi.dll. È incluso anche in Shlobj. h anziché in Shlwapi. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4,71 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
