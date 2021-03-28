---
description: Chiamato quando una finestra viene registrata come finestra della shell.
title: DShellWindowsEvents. WindowRegistered, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983067"
---
# <a name="dshellwindowseventswindowregistered-method"></a>DShellWindowsEvents. WindowRegistered, metodo

Chiamato quando una finestra viene registrata come finestra della shell.

## <a name="syntax"></a>Sintassi


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lCookie* \[ in\]
</dt> <dd>

Tipo: **Integer**

Cookie che identifica la finestra registrata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

A una finestra viene concesso un cookie quando viene registrato come finestra della shell. Per ulteriori informazioni, vedere [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Prodotto<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versione 5.00.2014.0216 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRevoked**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Registrazione**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**RegisterPending**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




