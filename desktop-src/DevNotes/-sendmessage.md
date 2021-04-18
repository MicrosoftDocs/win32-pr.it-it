---
description: Invia il messaggio specificato a una finestra o a finestre.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Funzione _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325676"
---
# <a name="_sendmessage-function"></a>\_SendMessage (funzione)

\[Questa funzione è un wrapper della funzione **SendMessage** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **SendMessage** .\]

Invia il messaggio specificato a una finestra o a finestre. Vedere [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Sintassi


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
