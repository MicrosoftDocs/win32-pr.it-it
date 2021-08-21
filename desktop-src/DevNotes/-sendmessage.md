---
description: Invia il messaggio specificato a una o più finestre.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage funzione
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
ms.openlocfilehash: bdd8a072970d8e6fb5e9af082f6f220531539a1c0061a7688d48be30dd659a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572571"
---
# <a name="_sendmessage-function"></a>\_Funzione SendMessage

\[Questa funzione è un wrapper sulla **funzione SendMessage.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono **chiamare direttamente SendMessage.**\]

Invia il messaggio specificato a una o più finestre. Vedere [**SendMessage.**](/windows/win32/api/winuser/nf-winuser-sendmessage)

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

 

 
