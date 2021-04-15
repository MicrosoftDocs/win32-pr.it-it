---
description: Riceve gli eventi di registrazione della finestra IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Oggetto DShellWindowsEvents (Exdisp. h)
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
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983014"
---
# <a name="dshellwindowsevents-object"></a>Oggetto DShellWindowsEvents

Riceve gli eventi di registrazione della finestra [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .

## <a name="members"></a>Membri

L'oggetto **dshellwindowsevents** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **dshellwindowsevents** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Chiamato quando una finestra viene registrata come finestra della shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Chiamato quando viene revocata la registrazione di una finestra della shell. <br/> |



 

## <a name="remarks"></a>Commenti

Usare **dshellwindowsevents** per monitorare la registrazione o la revoca di una finestra della shell. Per ulteriori informazioni, vedere [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Prodotto<br/> | Internet Explorer 5<br/>                                                                                           |
| Intestazione<br/>  | <dl> <dt>Exdisp. h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt> </dl> |
| IID<br/>     | \_ISHELLWINDOWS IID<br/>                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




