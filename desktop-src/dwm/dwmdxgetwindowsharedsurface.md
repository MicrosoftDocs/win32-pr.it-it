---
description: Recupera la superficie condivisa DirectX che esegue il backup di una finestra specificata. Per aggiornare il contenuto della finestra, è possibile scrivere questa superficie.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface (funzione)
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
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309434"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>DwmDxGetWindowSharedSurface (funzione)

Recupera la superficie condivisa DirectX che esegue il backup di una finestra specificata. Per aggiornare il contenuto della finestra, è possibile scrivere questa superficie.

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

[**HWND**](/windows/desktop/winprog/windows-data-types) che specifica la finestra da aggiornare.

`luidAdapter`

[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) dell'adapter in cui deve trovarsi la superficie.

`hmonitorAssociation`

Riservato.

`dwFlags`

Questo parametro può essere uno dei valori seguenti oppure una combinazione OR bit per bit di più valori laddove appropriato.

| Valore | Significato |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ \_ \_ Attesa del flag di reindirizzamento**</dt> <dt>0</dt> </dl> | Fa in modo che la funzione blocchi fino a quando non viene superata una sincronizzazione verticale (VSync) dall'ultima volta che la funzione è stata chiamata correttamente. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ \_Supporto del flag \_ di Reindirizzamento \_ presente \_ alla \_ \_ superficie GDI**</dt> <dt>0x10</dt> </dl> | Indica che l'applicazione chiamante è in grado di presentare a una superficie condivisa GDI. |

`pfmtWindow`

In input, il formato desiderato della superficie. Nell'output, il formato effettivo della superficie restituita.

`phDxSurface`

Nell'output, l'handle condiviso per la superficie.

`puiUpdateId`

Nell'output, ID dell'aggiornamento.

## <a name="return-value"></a>Valore restituito

Questa funzione può restituire uno di questi valori.

| Codice restituito | Descrizione |
|-|-|
| **\_OK** | La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie, assicurandosi di passare l'ID aggiornamento a [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (nel membro **PresentHistoryToken** della struttura di **\_ rendering D3DKMT** quando viene inviato l'aggiornamento e quindi [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) deve essere chiamato con lo stesso ID di aggiornamento. Si noti che **DwmDxUpdateWindowSharedSurface** deve essere chiamato indipendentemente dal fatto che la superficie sia stata effettivamente aggiornata o meno. |
| **\_superficie di \_ \_ Reindirizzamento GDI \_ di DWM** | La chiamata ha avuto esito positivo ed è necessario aggiornare la superficie chiamando [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)e impostando il **modello** del membro **PresentHistoryToken** su **D3DKMT \_ PM \_ reindirizzato \_ BLT** e specificando l'ID dell'aggiornamento nel membro **BLT** dell'Unione. Questo valore viene restituito solo se in *dwFlags* è stato specificato il **\_ supporto del \_ flag di reindirizzamento DWM presente nella \_ \_ \_ \_ \_ superficie GDI** . |
| **\_Adapter DWM \_ E \_ non \_ trovato** | Il valore di *luidAdapter* non è valido. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM non è attualmente abilitato e l'applicazione deve presentare un altro modo. |

## <a name="remarks"></a>Commenti

Questa API è destinata all'implementazione di un driver o di un runtime di grafica. Un'applicazione non può chiamare questo metodo. Questa documentazione è valida solo per Windows 7 e questa API non esiste né si comporta in modo analogo in altre versioni di Windows. Questa funzione non è presente in alcuna intestazione o libreria a collegamento statico e si trova in corrispondenza dell'ordinale 100 in dwmapi.dll.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | \[Solo app desktop di Windows 7\] |
| Server minimo supportato | Nessuno supportato |
| Fine del supporto client | Windows 7 |
| Intestazione | N/D |
| DLL | Dwmapi.dll |
