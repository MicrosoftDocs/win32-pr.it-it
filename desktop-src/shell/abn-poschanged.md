---
description: Notifica a una barra delle app quando si è verificato un evento che può influire sulle dimensioni e sulla posizione della barra dell'app.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: ABN_POSCHANGED messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92528de38b60c1f4705873427616b1ed7a5be6be5875a21e352d2136313c84df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943601"
---
# <a name="abn_poschanged-message"></a>Messaggio \_ POSCHANGED ABN

Notifica a una barra delle app quando si è verificato un evento che può influire sulle dimensioni e sulla posizione della barra dell'app. Gli eventi includono modifiche alle dimensioni, alla posizione e allo stato di visibilità della barra delle applicazioni, nonché l'aggiunta, la rimozione o il ridimensionamento di un'altra barra delle app sullo stesso lato dello schermo.


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Una barra delle app deve rispondere a questo messaggio di notifica inviando i messaggi [**\_ ABM QUERYPOS**](abm-querypos.md) [**e ABM \_ SETPOS.**](abm-setpos.md) Se la posizione è cambiata, la barra delle app deve chiamare [**la funzione MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) per spostarsi nella nuova posizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

