---
description: Recupera la superficie condivisa DirectX che si backupa una determinata finestra. Questa superficie può essere scritta in per aggiornare il contenuto della finestra.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: Funzione DwmDxGetWindowSharedSurface
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 47f8c75ee55521c0f1da4151f5161cf44a63dc51aab5658edbca288cb8edce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280131"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>Funzione DwmDxGetWindowSharedSurface

Recupera la superficie condivisa DirectX che si backupa una determinata finestra. Questa superficie può essere scritta in per aggiornare il contenuto della finestra.

## <a name="syntax"></a>Sintassi

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>Parametri

`hwnd`

[**HWND che**](/windows/desktop/winprog/windows-data-types) specifica la finestra da aggiornare.

`luidAdapter`

LUID [**dell'adapter**](/previous-versions/bb401655(v%3dmsdn.10)) in cui deve trovarsi la superficie.

`hmonitorAssociation`

Riservato.

`dwFlags`

Questo parametro può essere uno dei valori seguenti oppure una combinazione OR bit per bit di più valori, se appropriato.

| Valore | Significato |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ ATTESA \_ FLAG DI \_ REINDIRIZZAMENTO**</dt> <dt>0</dt> </dl> | Fa sì che la funzione si blocchi fino al termine di una sincronizzazione verticale (VSync) dall'ultima chiamata della funzione. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ SUPPORTO DEL \_ FLAG \_ DI \_ \_ REINDIRIZZAMENTO PRESENTE NELLA SUPERFICIE \_ GDI \_**</dt> <dt>0X10</dt> </dl> | Indica che l'applicazione chiamante è in grado di presentare a una superficie condivisa GDI. |

`pfmtWindow`

Nell'input, il formato desiderato della superficie. Nell'output, il formato effettivo della superficie restituita.

`phDxSurface`

Nell'output, handle condiviso per la superficie.

`puiUpdateId`

Nell'output, ID dell'aggiornamento.

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.

| Codice restituito | Descrizione |
|-|-|
| **S \_ OK** | La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie, assicurando di passare l'ID aggiornamento a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (nel membro **PresentHistoryToken** della struttura **RENDER D3DKMT \_** quando viene inviato l'aggiornamento e quindi [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve essere chiamato con lo stesso ID di aggiornamento. Si noti **che DwmDxUpdateWindowSharedSurface** deve essere chiamato indipendentemente dal fatto che la superficie sia stata effettivamente aggiornata o meno. |
| **SUPERFICIE DI \_ REINDIRIZZAMENTO \_ GDI \_ DWM S \_** | La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie chiamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e impostando Model del membro **PresentHistoryToken** su **D3DKMT \_ PM \_ REDIRECTED \_ BLT** e specificando l'ID di aggiornamento nel membro **Blt** dell'unione.  Questo valore viene restituito solo **se DWM \_ REDIRECTION \_ FLAG SUPPORT PRESENT \_ TO \_ \_ \_ GDI \_ SURFACE** è stato specificato in *dwFlags*. |
| **SCHEDA DWM \_ E \_ NON \_ \_ TROVATA** | Il valore di *luidAdapter* non è valido. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM non è attualmente abilitato e l'applicazione dovrà presentare un altro modo. |

## <a name="remarks"></a>Commenti

Questa API è destinata all'implementazione di un driver di grafica o di un runtime. Un'applicazione potrebbe non chiamare questo metodo. Questa documentazione è valida solo per Windows 7 e non è garantito che questa API esista o si comporti in modo simile in altre versioni di Windows. Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova al numero ordinale 100 in dwmapi.dll.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 7 \[ app desktop\] |
| Server minimo supportato | Nessuno supportato |
| Fine del supporto client | Windows 7 |
| Intestazione | N/D |
| DLL | Dwmapi.dll |
