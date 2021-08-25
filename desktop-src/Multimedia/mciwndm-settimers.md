---
title: MCIWNDM_SETTIMERS messaggio (Vfw.h)
description: Il messaggio MCIWNDM SETTIMERS imposta i periodi di aggiornamento usati da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra \_ padre.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- MCIWNDM_SETTIMERS messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807557"
---
# <a name="mciwndm_settimers-message"></a>Messaggio MCIWNDM \_ SETTIMERS

Il **messaggio MCIWNDM \_ SETTIMERS** imposta i periodi di aggiornamento usati da MCIWnd per aggiornare il trackbar nella finestra MCIWnd, aggiornare le informazioni sulla posizione visualizzate nella barra del titolo della finestra e inviare messaggi di notifica alla finestra padre. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetTimers.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*Attivo*
</dt> <dd>

Periodo di aggiornamento usato da MCIWnd quando è la finestra attiva. Il valore predefinito è 500 millisecondi. Archiviazione per questo valore è limitato a 16 bit.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*Inattivo*
</dt> <dd>

Periodo di aggiornamento usato da MCIWnd quando è la finestra inattiva. Il valore predefinito è 2000 millisecondi. Archiviazione per questo valore è limitato a 16 bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





