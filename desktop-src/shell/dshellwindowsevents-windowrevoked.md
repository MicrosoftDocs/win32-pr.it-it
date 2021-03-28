---
description: Chiamato quando viene revocata la registrazione di una finestra della shell.
title: DShellWindowsEvents. WindowRevoked, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983083"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>DShellWindowsEvents. WindowRevoked, metodo

Chiamato quando viene revocata la registrazione di una finestra della shell.

## <a name="syntax"></a>Sintassi


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lCookie* \[ in\]
</dt> <dd>

Tipo: **Integer**

Cookie che identifica la finestra revocata.

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

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Revoke**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




