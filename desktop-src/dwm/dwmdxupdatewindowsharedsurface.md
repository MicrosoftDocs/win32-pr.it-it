---
description: Notifica a DWM un aggiornamento in ingresso a una superficie condivisa della finestra.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface (funzione)
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
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528129"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>DwmDxUpdateWindowSharedSurface (funzione)

Notifica a DWM un aggiornamento in ingresso a una superficie condivisa della finestra.

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

[**HWND**](/windows/desktop/winprog/windows-data-types) che specifica la finestra da aggiornare.

`uiUpdateId`

ID aggiornamento recuperato da [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Riservato.

`hmonitorAssociation`

Riservato.

`prc`

Rect della finestra da aggiornare, nello spazio delle coordinate della finestra. Un rettangolo NULL indica che non è stata aggiornata alcuna area.

## <a name="return-value"></a>Valore restituito

**S \_ OK** se ha esito positivo, in caso contrario un HRESULT non riuscito **.**

## <a name="remarks"></a>Commenti

Questa API è destinata all'implementazione di un driver o di un runtime di grafica. Un'applicazione non può chiamare questo metodo. Questa documentazione è valida solo per Windows 7 e questa API non esiste né si comporta in modo analogo in altre versioni di Windows. Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova in corrispondenza dell'ordinale 101 in dwmapi.dll.

Questo metodo deve essere chiamato solo dopo che [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) restituisce **S \_ OK** e deve essere chiamato in tale scenario, indipendentemente dal fatto che la superficie venga aggiornata o meno.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | \[Solo app desktop di Windows 7\] |
| Server minimo supportato | Nessuno supportato |
| Fine del supporto client | Windows 7 |
| Intestazione | N/D |
| DLL | Dwmapi.dll |
