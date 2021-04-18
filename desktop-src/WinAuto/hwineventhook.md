---
title: HWINEVENTHOOK (windef. h)
description: Utilizzato per dichiarare una funzione hook dell'evento Window.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301683"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

Utilizzato per dichiarare una funzione hook dell'evento Window.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Commenti

Questo tipo di dati viene utilizzato con la funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e le funzioni [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                          |
| Componente ridistribuibile<br/>          | Active Accessibility 1,3 RDK in Windows NT 4,0 con SP6 e versioni successive e Windows 95<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Windef. h (WINVER >= 0x0500) (include Windows. h)</dt> </dl> |



 

 





