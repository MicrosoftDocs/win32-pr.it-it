---
description: Invia un messaggio al controllo specificato in una finestra di dialogo.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage funzione
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
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538837"
---
# <a name="_senddlgitemmessage-function"></a>\_Funzione SendDlgItemMessage

\[Questa funzione è un wrapper sulla **funzione SendDlgItemMessage.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono **chiamare direttamente SendDlgItemMessage.**\]

Invia un messaggio al controllo specificato in una finestra di dialogo. Vedere [**SendDlgItemMessage.**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

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

 

 
