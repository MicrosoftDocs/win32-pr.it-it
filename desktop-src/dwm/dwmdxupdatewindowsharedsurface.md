---
description: Notifica al DWM un aggiornamento in ingresso a una superficie condivisa della finestra.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: Funzione DwmDxUpdateWindowSharedSurface
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280121"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>Funzione DwmDxUpdateWindowSharedSurface

Notifica al DWM un aggiornamento in ingresso a una superficie condivisa della finestra.

## <a name="syntax"></a>Sintassi

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Parametri

`hwnd`

[**HWND che**](/windows/desktop/winprog/windows-data-types) specifica la finestra da aggiornare.

`uiUpdateId`

ID di aggiornamento recuperato [**da DwmDxGetWindowSharedSurface.**](dwmdxgetwindowsharedsurface.md)

`dwFlags`

Riservato.

`hmonitorAssociation`

Riservato.

`prc`

Il retto della finestra da aggiornare, nello spazio delle coordinate della finestra. Un rettangolo NULL indica che non è stata aggiornata alcuna area.

## <a name="return-value"></a>Valore restituito

**S \_ OK** in caso di esito positivo, in caso contrario un **HRESULT FAILED.**

## <a name="remarks"></a>Commenti

Questa API è destinata all'implementazione di un driver di grafica o di un runtime. Un'applicazione potrebbe non chiamare questo metodo. Questa documentazione è valida solo per Windows 7 e non è garantito che questa API esista o si comporti in modo simile in altre versioni di Windows. Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova in corrispondenza dell'ordinale 101 in dwmapi.dll.

Questo metodo deve essere chiamato solo dopo che [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) restituisce **S \_ OK** e deve essere chiamato in tale scenario, indipendentemente dal fatto che la superficie sia aggiornata o meno.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 7 \[ app desktop\] |
| Server minimo supportato | Nessuno supportato |
| Fine del supporto client | Windows 7 |
| Intestazione | N/D |
| DLL | Dwmapi.dll |
