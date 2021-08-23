---
description: Modifica il testo della barra del titolo della finestra specificata ( se ne ha una).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: a0c66230d9e7f074fe50ca826ab196ab75a239942257899362b738296b329074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572554"
---
# <a name="_setwindowtext-function"></a>\_Funzione SetWindowText

\[Questa funzione è un wrapper sulla **funzione SetWindowText.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono chiamare **direttamente SetWindowText.**\]

Modifica il testo della barra del titolo della finestra specificata ( se ne ha una). Vedere [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).

## <a name="syntax"></a>Sintassi


```C++
BOOL _SetWindowText(
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

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
