---
title: MCIWNDM_OPENINTERFACE messaggio (Vfw.h)
description: Il messaggio MCIWNDM OPENINTERFACE allega il flusso di dati o il file associato all'interfaccia specificata \_ a una finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83097ad6301dbfdb4636a8478c2df8e544207df334efd27fe9695f15e0693533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373517"
---
# <a name="mciwndm_openinterface-message"></a>Messaggio OPENINTERFACE MCIWNDM \_

Il **messaggio MCIWNDM \_ OPENINTERFACE** allega il flusso di dati o il file associato all'interfaccia specificata a una finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndOpenInterface.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*Punk*
</dt> <dd>

Puntatore a un'interfaccia IAVI che punta a un file o a un flusso di dati in un file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





