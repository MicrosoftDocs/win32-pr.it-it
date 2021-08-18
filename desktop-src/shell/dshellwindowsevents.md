---
description: Riceve gli eventi di registrazione della finestra IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Oggetto DShellWindowsEvents (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 13335268b892e4ac95520221fcd2e413c9c255225ccd8fc36c3c73cbf8c327a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009541"
---
# <a name="dshellwindowsevents-object"></a>Oggetto DShellWindowsEvents

Riceve gli [**eventi di registrazione della finestra IShellWindows.**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)

## <a name="members"></a>Membri

**L'oggetto DShellWindowsEvents** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto DShellWindowsEvents** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Chiamato quando una finestra viene registrata come finestra della shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Chiamato quando viene revocata la registrazione di una finestra della shell. <br/> |



 

## <a name="remarks"></a>Commenti

Usare **DShellWindowsEvents per** monitorare quando una finestra della shell viene registrata o revocata. Per altre informazioni, vedere [**IShellWindows.**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Prodotto<br/> | Internet Explorer 5<br/>                                                                                           |
| Intestazione<br/>  | <dl> <dt>Exdisp.h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




