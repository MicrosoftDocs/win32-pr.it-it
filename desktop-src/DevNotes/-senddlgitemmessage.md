---
description: Invia un messaggio al controllo specificato in una finestra di dialogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: Funzione _SendDlgItemMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325677"
---
# <a name="_senddlgitemmessage-function"></a>\_SendDlgItemMessage (funzione)

\[Questa funzione è un wrapper per la funzione **SendDlgItemMessage** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **SendDlgItemMessage** .\]

Invia un messaggio al controllo specificato in una finestra di dialogo. Vedere [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).

## <a name="syntax"></a>Sintassi


```C++
LRESULT _SendDlgItemMessage(
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

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
