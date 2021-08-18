---
description: Scarica la cache del database shim. Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: Funzione ShimFlushCache
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
ms.openlocfilehash: ecf1291b7fdcfb43170ec7e269fa140c321fafdbc09989fc7ee2b392f11c1160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075915"
---
# <a name="shimflushcache-function"></a>Funzione ShimFlushCache

Scarica la cache del database shim. Questa funzione deve essere chiamata dopo l'installazione di un nuovo database shim.

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

*hwnd* \[ in, facoltativo\]
</dt> <dd>

Non usato; deve essere 0.

</dd> <dt>

*hInstance* \[ in, facoltativo\]
</dt> <dd>

Non usato; deve essere 0.

</dd> <dt>

*lpszCmdLine* \[ in, facoltativo\]
</dt> <dd>

Non usato; deve essere 0.

</dd> <dt>

*nCmdShow* \[ Pollici\]
</dt> <dd>

Non usato; deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

## <a name="remarks"></a>Commenti

Il chiamante deve essere un amministratore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




