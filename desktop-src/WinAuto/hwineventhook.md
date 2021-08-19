---
title: HWINEVENTHOOK (Windef.h)
description: Usato per dichiarare una funzione hook dell'evento della finestra.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a26a2593af7db4520248b5ee319fd4143a79ab1393cef02365d1fe3ea8cc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994151"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Usato per dichiarare una funzione hook dell'evento della finestra.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Commenti

Questo tipo di dati viene usato con la funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e le [**funzioni SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e [**UnhookWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                          |
| Componente ridistribuibile<br/>          | Active Accessibility 1.3 RDK in Windows NT 4.0 con SP6 e versioni successive e Windows 95<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt> </dl> |



 

 





