---
description: Chiamato quando viene revocata la registrazione di una finestra della shell.
title: Metodo DShellWindowsEvents.WindowRevoked
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
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459848"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>Metodo DShellWindowsEvents.WindowRevoked

Chiamato quando viene revocata la registrazione di una finestra della shell.

## <a name="syntax"></a>Sintassi


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lCookie* \[ Pollici\]
</dt> <dd>

Tipo: **Integer**

Cookie che identifica la finestra revocata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

A una finestra viene concesso un cookie quando viene registrato come finestra shell. Per altre informazioni, vedere [**Registrare**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

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

[**Revocare**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




