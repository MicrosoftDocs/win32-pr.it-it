---
description: Svuota la cache del database shim. Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049078"
---
# <a name="shimflushcache-function"></a>ShimFlushCache (funzione)

Svuota la cache del database shim. Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in, facoltativo\]
</dt> <dd>

Inutilizzati deve essere 0.

</dd> <dt>

*HINSTANCE* \[ in, facoltativo\]
</dt> <dd>

Inutilizzati deve essere 0.

</dd> <dt>

*lpszCmdLine* \[ in, facoltativo\]
</dt> <dd>

Inutilizzati deve essere 0.

</dd> <dt>

*nCmdShow* \[ in\]
</dt> <dd>

Inutilizzati deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Il chiamante deve essere un amministratore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




