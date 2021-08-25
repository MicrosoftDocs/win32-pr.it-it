---
title: MCI_OVLY_WINDOW_PARMS struttura (Mciapi.h)
description: La struttura MCI OVLY WINDOW PARMS contiene informazioni di visualizzazione della finestra per il \_ \_ comando FINESTRA \_ MCI per i dispositivi con \_ sovrapposizione video.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS struttura Windows Multimediali
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd19580dacdc819f35bc36ed8f0070a5fc1b9fc4b745c78711c4fc312611e3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138285"
---
# <a name="mci_ovly_window_parms-structure"></a>Struttura PARMS FINESTRA MCI \_ OVLY \_ \_

La **struttura MCI \_ OVLY \_ WINDOW \_ PARMS** contiene informazioni di visualizzazione della finestra per il [**comando FINESTRA MCI \_**](mci-window.md) per i dispositivi con sovrapposizione video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCallback**
</dt> <dd>

La parola di ordine basso specifica un handle di finestra usato per il flag MCI \_ NOTIFY.

</dd> <dt>

**hWnd**
</dt> <dd>

Handle per visualizzare la finestra.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Comando di visualizzazione della finestra.

</dd> <dt>

**lpstrText**
</dt> <dd>

Didascalia della finestra.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel *parametro fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**FINESTRA \_ MCI**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

