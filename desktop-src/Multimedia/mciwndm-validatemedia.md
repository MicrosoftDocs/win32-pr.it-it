---
title: Messaggio di MCIWNDM_VALIDATEMEDIA (VFW. h)
description: Il \_ messaggio MCIWNDM VALIDATEMEDIA aggiorna le posizioni iniziale e finale del contenuto, la posizione corrente nel contenuto e l'oggetto TrackBar in base al formato dell'ora corrente.
ms.assetid: 98ac6227-fc90-4276-8e26-2bd005e35dc6
keywords:
- MCIWNDM_VALIDATEMEDIA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_VALIDATEMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cb6e6a4a7c320d4eb6472c3c72da2843d0814c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517410"
---
# <a name="mciwndm_validatemedia-message"></a>\_Messaggio MCIWNDM VALIDATEMEDIA

Il messaggio **MCIWNDM \_ VALIDATEMEDIA** aggiorna le posizioni iniziale e finale del contenuto, la posizione corrente nel contenuto e l'oggetto TrackBar in base al formato dell'ora corrente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia) .


```C++
MCIWNDM_VALIDATEMEDIA 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

In genere, non è necessario usare questa macro. Tuttavia, se l'applicazione modifica il formato dell'ora di un dispositivo senza usare MCIWnd; le posizioni iniziale e finale del contenuto, oltre a TrackBar, continuano a usare il vecchio formato. È possibile utilizzare questa macro per aggiornare questi valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)
</dt> </dl>

 

 





