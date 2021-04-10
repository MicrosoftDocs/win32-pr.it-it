---
title: Struttura MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: La \_ struttura parametri della finestra OVLY di MCI \_ \_ contiene informazioni sulla visualizzazione della finestra per il \_ comando della finestra MCI per i dispositivi con sovrimpressione video.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Struttura MCI_OVLY_WINDOW_PARMS di Windows Multimedia
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
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963742"
---
# <a name="mci_ovly_window_parms-structure"></a>\_ \_ Struttura parametri della finestra OVLY MCI \_

La **struttura \_ \_ \_ parametri della finestra OVLY di MCI** contiene informazioni sulla visualizzazione della finestra per il comando della [**\_ finestra MCI**](mci-window.md) per i dispositivi con sovrimpressione video.

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

La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.

</dd> <dt>

**hWnd**
</dt> <dd>

Handle per la finestra di visualizzazione.

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

Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Strutture MCI**](mci-structures.md)
</dt> <dt>

[**\_finestra MCI**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

