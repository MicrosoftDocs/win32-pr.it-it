---
title: Messaggio di ICM_DRAW_WINDOW (VFW. h)
description: Il \_ messaggio della \_ finestra di progetto ICM notifica a un driver di rendering che è \_ necessario ricreare la finestra specificata per il messaggio di inizio del progetto ICM \_ .
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476241"
---
# <a name="icm_draw_window-message"></a>Messaggio della finestra di \_ disegni ICM \_

Il messaggio della **\_ \_ finestra di progetto ICM** notifica a un driver di rendering che è necessario ricreare la finestra specificata per il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) . La finestra è stata spostata o diventa temporaneamente nascosta. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Puntatore al rettangolo di destinazione nelle coordinate dello schermo. Se questo parametro punta a un rettangolo vuoto, il disegno deve essere disattivato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è supportato da hardware che esegue la decompressione, la temporizzazione e il disegno asincroni.

I driver della sovrimpressione video usano questo messaggio per creare quando la finestra viene nascosta o spostata. Quando una finestra specificata per [**l' \_ \_ inizio di un progetto ICM**](icm-draw-begin.md) è completamente nascosta da altre finestre, il rettangolo di destinazione è vuoto. Quando si verifica questa condizione, i driver devono disattivare l'hardware con sovrimpressione video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





