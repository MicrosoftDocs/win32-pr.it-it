---
description: Visualizza la scheda Condivisione cartelle nella finestra delle proprietà per la cartella specificata.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Funzione ShowShareFolderUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968260"
---
# <a name="showsharefolderui-function"></a>Funzione ShowShareFolderUI

Visualizza la **scheda Condivisione** cartelle nella finestra delle proprietà per la cartella specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre per la finestra delle proprietà.

</dd> <dt>

*pszPath* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il percorso della cartella in cui viene visualizzata la **scheda Condivisione** cartelle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questa funzione restituisce sempre S \_ OK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file con estensione lib. Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
